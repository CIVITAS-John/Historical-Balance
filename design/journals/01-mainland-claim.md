# The Claim Across the Strait

The court must decide whether Tungning still speaks for the Ming cause. In 1836, Qing claims Taiwan, starts at −35 relations with Tungning, and embargoes it.

## Opening effects

- **Starting forces:** Tungning has ten early troopships and five frigates, plus five marine, eight line infantry, and two cannon artillery battalions raised in Taiwan. Qing has three frigates. These are part of the [1836 setup](../../common/scripted_effects/fh_tungning_setup.txt).
- **Disputed mandate:** While the court debates the claim, Tungning gets **−10 base legitimacy** and **−50% naval goods costs**. Established suppliers keep the fleet provisioned cheaply, but maintaining the army and paying both services still strain the indebted treasury.
- **Ends:** Remove both effects when the court reasserts, opens renunciation talks, or reaches the Taiping fork. The Qing offer and reassertion mobilization have their own effects.

## Mainland foothold

The objectives are **Fujian**, **Guangdong**, and **Zhejiang**. Check each Victoria 3 state region separately.

- **Counts:** Tungning directly owns all land in the region apart from treaty-port enclaves. It must own ordinary land in the region.
- **Exempt:** Actual treaty-port enclaves can remain in foreign hands. A designated port province held as ordinary territory is still required.
- **Does not count:** A treaty port alone, any other partial holding, occupation without ownership, or land held by a Tungning subject.
- **While the claim is unresolved:** The first foothold immediately settles the claim as **Reassert**. Check ownership before a bar endpoint, a Qing response, or the opening of the Taiping fork. Once the fork opens, the court must make that choice even if a foothold arrives while the event is pending.
- **After the claim is settled:** A foothold opens [The Return to the Mainland](06-mainland-reconquest.md#opening) if it has not opened already, unless the court permanently abandoned the project at the Taiping fork. It leaves the recorded stance and ratified treaties intact.
- **Shared check:** Use the same ownership rule for the follow-up and the [Ming restoration track](05-constitutional-settlement.md#ming-restoration). Use state-region ownership and actual treaty-port state status; a port marker alone does not identify an enclave.

## Court balance

- **Entry:** `fh_je_mainland_claim`, starting at **90/200**.
- **Endpoints:** **0** opens renunciation; **200** reasserts the claim. Check after every point change. The AI uses the same rules.
- **Taiping fork:** There is no calendar deadline. If the [Taiping Rebellion](08-taiping-rebellion.md#the-last-chance) starts while the claim is unsettled, freeze the bar and retire the ordinary court choices. A qualifying foothold already owned at that check still resolves first. If Taiping never rises, the court can still settle through the bar or ownership. If Qing disappears without the rebellion ever starting, drop Qing-specific drift and keep those routes available.
- **Monthly drift:**
  - −1 while Qing embargoes Tungning.
  - −1 while Qing has a cordial relationship with Tungning, or above.
  - −1 while Tungning uses at least 75% of its credit (`scaled_debt`).
  - −1 while Tungning is at war and not fighting Qing.
  - +1 while the Ming Estates are in government.
  - +1 if the Army and Fleet are in government with a mainland-first leader; −1 with a southern-expedition leader; zero otherwise.
  - +1 while a Jingoist leads another governing group. The Army and Fleet use only their own stance rule.
  - +1 while Qing is at a war.
  - +1 while Qing has a cold relationship with Tungning, or below.

### Court actions

Both actions share a six-month cooldown. The starting government can use either while the embargo holds. For each action, use the first eligible sponsor below. Skip any approval effect if its target is absent.

- **Read the Ming Memorials**
  - **Requires:** The governing Ming Estates, governing mainland-first Army and Fleet, or another governing group led by a Jingoist, Royalist, or Traditionalist (highest clout, fixed order on ties).
  - **Balance:** +12.
  - **Approval:** +2 for the supporter for six months.
  - **Disapproval:** −2 for the Maritime Houses for six months.
  - **Modifier:** +5% military goods costs for six months.
- **Hear the Strait Merchants**
  - **Requires:** The governing Maritime Houses, governing Petite Bourgeoisie, governing southern-expedition Army and Fleet, another governing group led by a Pacifist or Market Liberal (highest clout, fixed order on ties), or the governing Ming Estates while Qing’s embargo is in force.
  - **Balance:** −12.
  - **Approval:** +2 for the supporter for six months.
  - **Disapproval:** −2 for the Ming Estates for six months; skip that penalty if they sponsored the action to protect their exports.
  - **Modifier:** +10% trade advantage in Taiwan for six months.

### Court events

- **Roll:** Each quarter, a 10% chance to draw one eligible event.
- **Effects:** Each event offers choices of +5 or −5 to the bar and starts a 12-month event cooldown. Let a stronger intervention trade a longer preparatory effect for a larger immediate reaction. These effects apply on response; only a result that settles the claim grants the linked aftermath.

1. Canton merchants sharing a favor
2. Fujian officials proposes a deal
3. Tongning merchants petitioning
4. Young officers clamoring for action: a mainland-first leader asks for a Fujian expedition (+5 if heard); a southern-expedition leader asks to keep the squadron in the south (−5 if heard). Backing the officers publicly follows their preferred direction, immediately removes 2% radicals among Army and Fleet supporters, and adds 10% naval power projection and 5% military goods costs for one year. Refusing the petition moves the bar the other way and gives the group −2 approval for six months. Skip this event under a neutral leader and recheck the stance when answered.
5. Mainland refugees asking for liberation
6. Ming royal family's petition

## Reassert the claim

- When a court action or event answer would reach 200, let its confirmation offer a measured declaration or a public challenge. Use the measured declaration on monthly progress or qualifying ownership. At the Taiping fork, offer both versions of reassertion in the existing choice. The AI prefers a public challenge only with a mainland-first Army and Fleet in government and enough credit room (under 75% of credit used, out of default).
- Record `reclaim` and `mainland_settled`, close the journal, and apply the chosen [mainland aftermath](outcome-modifiers.md#mainland-claim).
- Add Tungning claims on any of the three regions that do not already meet the foothold rule.
- Open [The Return to the Mainland](06-mainland-reconquest.md#opening) and start [mobilization](06-mainland-reconquest.md#mobilization-after-reassertion) once, including when a foothold prompted the decision. Boost army and navy combat readiness and reduce investment pool contributions by 50% for the duration.
- Unlock [Press the Mainland Claims](06-mainland-reconquest.md#decision-press-the-mainland-claims) to pursue the outstanding coastal claims.
- When mobilization ends, unlock the constitutional debate. Reassertion makes the Ming route possible; it does not choose a dynasty.

## Renounce the claim

### Offer and response

- **Opening:** Freeze the court debate and make at most one offer. Keep the journal visible while renunciation is provisional and show that it is waiting for Qing.
- **AI Qing:** Ratify immediately if eligible.
- **Player-controlled Qing:** Allow 90 days to respond. Expiry counts as refusal.
- **No deal:** Finish with renunciation if Qing no longer exists, is at war with Tungning, lacks the rank or country type to take a tributary, or cannot grant all terms. Also decline if Tungning serves another overlord. Reuse an existing direct Qing tributary relationship; never transfer a third party’s subject by script.
- **Blocked trade article:** Show why the full offer is unavailable before the endpoint where possible. Full Isolationism or an incompatible market arrangement can block ratification. An equivalent existing directed article fulfills this term.
- **Interruptions:** A foothold gained before ratification cancels the offer and reasserts the claim. The Taiping fork cancels the offer if no foothold qualifies. Any response or timeout for a canceled offer has no effect.

### Effects of final renunciation

- On ratification, refusal, expiry, or an unavailable deal, record `renounce` and `mainland_settled` and close the journal. A canceled offer due to reconquest does not count as renunciation.
- Remove Tungning’s claims on Fujian, Guangdong, and Zhejiang.
- Apply the matching [renunciation aftermath](outcome-modifiers.md#mainland-claim) after the offer’s final status is known.
- Unlock the constitutional debate with the Ming track permanently closed.
- On refusal, expiry, or failure to agree, record the reason and leave existing diplomacy intact.
- **Taiping abandonment:** Use the fork’s renunciation result without making another Qing offer. Also permanently close the scripted foothold, reunification, and Taiping-aid routes. This leaves ordinary diplomacy and war goals available.

### Terms on ratification

- Make Tungning a direct Qing tributary or reuse that relationship.
- Halve the normal tribute with the scoped vanilla multiplier, which does not require the DLC subject interaction. A nominal 20% becomes 10% before other modifiers. Keep the discount only while Tungning is a direct Qing tributary under this agreement.
- Grant five years of **Qing → Tungning trade privileges**. Keep separate markets as needed so Tungning receives the access.
- Remove Qing’s embargo and raise relations to at least +30.
- Preserve Tungning’s colonial holdings and direct subjects, and Qing’s claim on Taiwan.

### Ratification sequence

Use one offer handler for AI acceptance, player responses, and expiry. Ignore later responses or timeouts once the offer has been consumed or canceled.

1. Check for a foothold and an already launched Taiping Rebellion first, then recheck rank, peace, tribute, markets, and article eligibility, including the expected effects of becoming a tributary.
2. Consume the pending offer and record the current embargo, pacts, and market arrangement.
3. Remove the embargo, establish or reuse the tributary relationship, secure a separate market for Tungning if needed, and create or reuse the directed article.
4. Verify the resulting pacts before applying the discount and relations change. If a term fails, roll back only this offer’s changes, restore the embargo if still legal, and finalize renunciation without a deal.
5. Recheck the tribute discount when the overlord or subject type changes.

## Static checks

- Check that either endpoint removes both opening effects, including while an offer is pending. The naval discount must not reduce army goods costs or military wages.
- Trace both endpoints, an unresolved bar that survives past 1846, Qing disappearing without Taiping rising, and a foothold that takes precedence over the bar or the opening of the fork.
- Trace an eligible AI deal, player acceptance and refusal, expiry, an invalid offer, and ratification with no existing embargo.
- Check that a foothold or the fork cancels a pending offer once and has no effect on a finalized deal.
- Check that breaking the tributary relationship removes the discount.
- Vanilla references: `common/subject_types/00_subject_types.txt`, `common/diplomatic_actions/24_subject_tributary.txt`, `common/modifier_type_definitions/00_modifier_types.txt`, and `common/treaty_articles/25_trade_privilege.txt`. Qing’s Canton System is distinct from full Isolationism.
