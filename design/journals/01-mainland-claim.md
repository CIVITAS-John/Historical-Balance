# The Claim Across the Strait

The court must decide whether Tungning still speaks for the Ming cause. In 1836, Qing claims Taiwan, starts at −35 relations with Tungning, and embargoes it.

## Opening effects

- **Starting forces:** Tungning has ten early troopships and five frigates, plus five marine, eight line infantry, and two cannon artillery battalions raised in Taiwan. Qing has three frigates. These are part of the [1836 setup](../../common/scripted_effects/fh_tungning_setup.txt).
- **Disputed mandate:** While the court debates the claim, Tungning gets **−10 base legitimacy** and **−50% naval goods costs**. Established suppliers keep the fleet provisioned cheaply, but maintaining the army and paying both services still strain the indebted treasury.
- **Ends:** Remove both effects when the court reasserts or opens renunciation talks. The Qing offer and the reassertion mobilization have their own effects.

## Mainland foothold

The objectives are **Fujian**, **Guangdong**, and **Zhejiang**. Check each Victoria 3 state region separately.

- **Counts:** Tungning directly owns all land in the region apart from treaty-port enclaves. It must own ordinary land in the region.
- **Exempt:** Actual treaty-port enclaves can remain in foreign hands. A designated port province held as ordinary territory is still required.
- **Does not count:** A treaty port alone, any other partial holding, occupation without ownership, or land held by a Tungning subject.
- **While the claim is unresolved:** The first foothold immediately settles the claim as **Reassert**, regardless of the bar or deadline. Check ownership before resolving a bar endpoint, deadline, or Qing response.
- **After the claim is settled:** A first foothold still opens [The Return to the Mainland](06-mainland-reconquest.md). It does not change the recorded stance or any ratified treaty.
- **Shared check:** Use the same ownership rule for the follow-up and the [Ming restoration track](05-constitutional-settlement.md#ming-restoration). Use state-region ownership and actual treaty-port state status; a port marker alone does not identify an enclave.

## Court balance

- **Entry:** `fh_je_mainland_claim`, starting at **90/200**.
- **Endpoints:** **0** opens renunciation; **200** reasserts the claim. Check after every point change. The AI uses the same rules.
- **Deadline:** On the 10th anniversary, choose the nearer endpoint. A tie goes to renunciation. The deadline still applies if court actions keep the bar near the middle.
- **Monthly drift:**
  - −1 while Qing embargoes Tungning.
  - −1 while Qing has a cordial relationship with Tungning, or above.
  - −1 while Tungning uses at least 75% of its credit (`scaled_debt`).
  - -1 while Tungning is at a war and is not with Qing.
  - +1 while the Armed Forces is in government.
  - +1 while a Jingoist leads any government groups.
  - +1 while Qing is at a war.
  - +1 while Qing has a cold relationship with Tungning, or below.

### Court actions

Both actions share a six-month cooldown. The starting government can use either while the embargo holds. If several groups qualify for an action, apply approval once to the named supporter.

- **Read the Ming Memorials**
  - **Requires:** Governing groups led by a Jingoist, Royalist, or Traditionalist.
  - **Balance:** +12.
  - **Approval:** +2 for the supporter for six months.
  - **Disapproval:**: -2 for the other side for six months.
  - **Modifier:** +5% military goods costs for six months.
- **Hear the Strait Merchants**
  - **Requires:** Governing Industrialists or Petite Bourgeoisie; any governing Pacifist or Market Liberal leader; or governing Landowners while Qing’s embargo is in force.
  - **Balance:** −12.
  - **Approval:** +2 for the supporter for six months.
  - **Disapproval:**: -2 for the other side for six months.
  - **Modifier:** +10% trade advantage in Taiwan for six months.

### Court events

- **Roll:** Each quarter, a 10% chance to draw one eligible event.
- **Effects:** Each event offers a choice between +5 and 5, with a minor timed modifiers, and starts a 12-month event cooldown.

1. Canton merchants sharing a favor
2. Fujian officials proposes a deal
3. Tongning merchants petitioning
4. Young officers clamoring for action
5. Mainland refugees asking for liberation
6. Ming royal family's petition

## Reassert the claim

- Record `reclaim` and `mainland_settled` and close the journal.
- Add Tungning claims on any of the three regions that do not already meet the foothold rule.
- If Qing still exists, reduce relations by 60 points, down to the vanilla floor.
- Should change AI strategy to build more military.
- For three years:
  - Give the Armed Forces and Landowners +5 approval and the Industrialists -5.
  - Boost land/naval offense, defense, morale recovery, while making investment pool -50%.
  - The modifier stops once the Qing war is started and completed.
  - If the modifier stops without a Qing war happened, add a negative event with timed modifiers.
  - If the war fails, add another negative event with timed modifiers.
- Once the modifier is gone:
  - Unlock the constitutional debate. Reassertion makes the Ming route possible; it does not choose a dynasty.
- Enables a decision to declare war on Qing for the three provinces without infamy.
  - AI should use it when Qing is at war or has significant internal turmoil, plus when it has army.
- If a foothold prompted the decision, open the reconquest journal in the same check.
  - Add the timed modifier.

## Renounce the claim

### Offer and response

- **Opening:** Close the court debate and make at most one offer. Renunciation remains provisional until the offer is resolved.
- **AI Qing:** Ratify immediately if eligible.
- **Player-controlled Qing:** Allow 90 days to respond. Expiry counts as refusal.
- **No deal:** Finish with renunciation if Qing no longer exists, is at war with Tungning, lacks the rank or country type to take a tributary, or cannot grant all terms. Also decline if Tungning serves another overlord. Reuse an existing direct Qing tributary relationship; never transfer a third party’s subject by script.
- **Blocked trade article:** Show why the full offer is unavailable before the endpoint where possible. Full Isolationism or an incompatible market arrangement can block ratification. An equivalent existing directed article fulfills this term.
- **Conquest while pending:** If Tungning gains a foothold before ratification, cancel the offer and reassert the claim. Any later response or timeout has no effect.

### Effects of final renunciation

- On ratification, refusal, expiry, or an unavailable deal, record `renounce` and `mainland_settled` and close the journal. A canceled offer due to reconquest does not count as renunciation.
- Remove Tungning’s claims on Fujian, Guangdong, and Zhejiang.
- For three years, give the Industrialists +2 approval and the Armed Forces −2.
- Unlock the constitutional debate with the Ming track permanently closed.
- On refusal, expiry, or failure to agree, record the reason and leave existing diplomacy intact.

### Terms on ratification

- Make Tungning a direct Qing tributary or reuse that relationship.
- Halve the normal tribute with the scoped vanilla multiplier, which does not require the DLC subject interaction. A nominal 20% becomes 10% before other modifiers. Keep the discount only while Tungning is a direct Qing tributary under this agreement.
- Grant five years of **Qing → Tungning trade privileges**. Keep separate markets as needed so Tungning receives the access.
- Remove Qing’s embargo and raise relations to at least +30.
- Preserve Tungning’s colonial holdings and direct subjects, and Qing’s claim on Taiwan.

### Ratification sequence

Use one offer handler for AI acceptance, player responses, and expiry. Ignore later responses or timeouts once the offer has been consumed or canceled.

1. Recheck rank, peace, tribute, markets, and article eligibility, including the expected effects of becoming a tributary.
2. Consume the pending offer and record the current embargo, pacts, and market arrangement.
3. Remove the embargo, establish or reuse the tributary relationship, secure a separate market for Tungning if needed, and create or reuse the directed article.
4. Verify the resulting pacts before applying the discount and relations change. If a term fails, roll back only this offer’s changes, restore the embargo if still legal, and finalize renunciation without a deal.
5. Recheck the tribute discount when the overlord or subject type changes.

## Static checks

- Check that either endpoint removes both opening effects, including while an offer is pending. The naval discount must not reduce army goods costs or military wages.
- Trace each bar endpoint, the deadline and tie, and a foothold that takes precedence over them.
- Trace an eligible AI deal, player acceptance and refusal, expiry, an invalid offer, and ratification with no existing embargo.
- Check that a foothold cancels a pending offer once and has no effect on a finalized deal.
- Check that breaking the tributary relationship removes the discount.
- Vanilla references: `common/subject_types/00_subject_types.txt`, `common/diplomatic_actions/24_subject_tributary.txt`, `common/modifier_type_definitions/00_modifier_types.txt`, and `common/treaty_articles/25_trade_privilege.txt`. Qing’s Canton System is distinct from full Isolationism.
