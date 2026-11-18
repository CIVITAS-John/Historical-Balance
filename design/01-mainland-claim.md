# The Claim Across the Strait

The court must decide whether it still speaks for the Ming cause. In 1836, Qing already claims Taiwan, starts at −35 relations with Tungning, and embargoes it (`common/scripted_effects/fh_tungning_setup.txt:183–189`).

## Court balance

`fh_je_mainland_claim` begins at **45/100**. **0** means renounce the claim; **100** means reclaim. On every point change, the court immediately commits at either endpoint. A fifth anniversary deadline commits to the nearer endpoint; an exact tie defaults to renunciation. AI takes the same endpoints.

| Source | Change |
| --- | --- |
| Each month with the Qing embargo or Tungning using at least 75% of its credit (`scaled_debt`) | −1 each |
| Each month with a Jingoist leader of the Armed Forces in government, or with Tungning holding a full mainland objective region | +1 each |
| **Read the Ming Memorials**: governing Landowners under Monarchy, or governing Armed Forces led by a Jingoist or Royalist | +12; gives the acting group +2 approval and raises naval goods costs by 5% for six months |
| **Hear the Strait Merchants**: governing Industrialists or Petite Bourgeoisie, any governing Pacifist or Market Liberal leader, or governing Landowners facing the embargo | −12; gives the acting group +2 approval and local trade capacity +5% in Taiwan for six months |

Court actions share a six-month cooldown. The starting government can use either action while the embargo holds, but persistently high debt makes reconciliation harder to resist. The court can keep balances close but cannot delay the fifth anniversary. If several groups qualify for the same action, the named supporter receives the effect once.

Each quarter, roll a 20% chance to draw one eligible event: merchant petitions while embargoed and above the credit threshold, retired officers’ petitions after the fleet grows by two warships, or a refugee memorial when Qing-controlled Fujian has at least 15% turmoil. Each offers a ±4 choice and starts a 12-month event cooldown. An unanswered event expires without moving the bar. An event still open at settlement can no longer change its course.

## The two outcomes

**Reassert the claim.** Add Tungning claims to Fujian, Guangdong, and Zhejiang where Tungning does not already own the full region. If Qing is alive, reduce current Qing relations by **60 points** down to the vanilla floor; no war starts and the embargo stays as it is. For three years give the Armed Forces and Landowners +2 approval and the Industrialists −2. Record the mainland stance as `reclaim` and finish the journal immediately. This makes the Ming path possible later; it does not pick the dynasty.

**Renounce the claim.** Immediately record `renounce` and remove any Tungning claims on the three objective regions. For three years give the Industrialists +2 approval and the Armed Forces −2. Qing’s offer exchanges the renunciation for direct tributary status, **half the normal tribute** and five years of **Qing → Tungning trade privileges**. Remove Qing’s embargo and raise Qing relations to at least +30 on ratification. Preserve Tungning’s colonial holdings and direct subjects. Keep separate markets where needed so the article works; the agreement grants Tungning access, not the reverse. Qing’s claim on Taiwan remains.

- With eligible AI Qing, ratify immediately. If Qing is player controlled, the offer expires after 90 days, defaulting to refusal. Tungning’s renunciation is already final while the offer is pending.
- If Qing is gone, at war with Tungning, lacks the rank or country type to take a tributary, or Tungning serves another overlord, finish with renunciation and no treaty. Refusal or timeout likewise leaves the existing diplomacy intact. State the reason in the journal. For an existing direct Qing tributary, reuse the relationship. Never transfer a third party’s subject by script.
- If the subject and discount are legal but a trade article is blocked (for example by full Isolationism or another market arrangement the mod cannot undo), Qing’s offer does not ratify. Show the reason before the endpoint where possible; do not present a lesser deal as full settlement. Treat an equivalent existing directed article as fulfilling the condition.
- Use the scoped vanilla tribute multiplier for the discount so the deal works without the DLC-gated subject interaction. Apply −50% to Tungning’s contribution only while it is a direct Qing tributary under this agreement; 20% becomes nominally 10% before other modifiers. Recheck and remove the discount on a change of overlord or subject type.

Use one pending offer and one ratification effect for AI, a player response, and expiry. On acceptance, recheck rank, peace, tribute, markets, and article eligibility, including changes that would result from becoming a tributary. Consume the offer before applying effects. Record the existing embargo, pacts, and market arrangement; then remove the embargo, establish or reuse the tributary, secure Tungning’s own market if needed, and create or reuse the directed article. Verify the resulting pacts before applying the discount and relations reward. If a script effect cannot produce the terms, roll back only changes this offer made, restoring the embargo if still legal, and leave the stance as renounced without a deal. A later response or timeout has no effect once the offer is consumed.

Set `mainland_settled` on reassertion, ratification, refusal, expiry, or no possible agreement. The constitutional journal checks this flag rather than the bar value. Test normal 1836 ratification, a human Qing response, no valid Qing deal, the embargo already gone, and a subject breaking away after the discount. Vanilla references: `common/subject_types/00_subject_types.txt:127–177`, `common/diplomatic_actions/24_subject_tributary.txt:11–26`, `common/modifier_type_definitions/00_modifier_types.txt:232–239`, and `common/treaty_articles/25_trade_privilege.txt:34–65`. Qing’s starting Canton System is distinct from full Isolationism.
