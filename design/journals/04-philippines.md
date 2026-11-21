# The Manila Question

The Manila Compact was a bargain with Spain. If Manila breaks away, Tungning can offer protection on terms that leave Manila in charge of its own market, or press its demands through a normal diplomatic play.

## Opening

- **Entry:** `fh_je_manila_question`. Show it while the Philippines (`PHI`) owns Manila city (`p:x0D8236`) and Spain is absent from its entire overlord chain.
- **Window:** Start the eight-year clock the first time an independent Philippines meets those conditions. If it serves another power, show why the opportunity is blocked. An annexed Philippines cannot open it.
- **Suspension:** If Manila changes hands or the Philippines loses independence, check first for qualifying Tungning submission or conquest. Otherwise suspend new actions and cancel pending offers and events until independent `PHI` again owns Manila. The clock keeps running and cannot restart.

## Court actions

- **Offer the Manila Charter:** Ask Manila to accept Tungning as its overlord in exchange for keeping its own market. Require peace, no opposing diplomatic play, an active interest in Indonesia, at least +30 relations, and a trade privileges or investment rights agreement already in force between the two countries. Manila must control its own market and qualify for a native Tributary or Protectorate pact under Tungning. Send one offer per journal and give Manila 30 days to answer. On acceptance, recheck eligibility and apply the subject pact and native **Grant Own Market** together. Record peaceful submission only after both terms take effect. The grant has its normal minimum term and liberty desire cost for revocation. Refusal, timeout, or failure to deliver both terms leaves the existing relationship in place.
- **Provision the Expedition:** Once a qualifying play has become a war, spend **5% of Tungning’s gold reserve cap** on landing stores. Require enough cash to pay the full cost, no default, and no other active war. Tungning gains **+20% naval invasion efficiency** for six months. End the bonus if the recorded war ends, Tungning enters another war, or the journal suspends or closes. An expedition already funded can keep its remaining term during a deadline hold. Fund it once per journal; the player chooses when the fleet is ready to use it.

Ordinary diplomacy and native demands remain available without either action. Neither action extends the deadline, and neither can start during a deadline hold.

## Events

Each quarter during the open window, roll a 10% chance to draw one eligible event. Start a shared 12-month cooldown on draw. These petitions concern trade, relief, and land use, so either approach can face them. Require Tungning to own a state in Taiwan, and recheck ownership and event eligibility on response. A petition can be resolved once per journal. Let it pass without effect if dismissed, unanswered after 30 days, or still pending when a suspension, deadline hold, or closure begins.

| Event | Eligible while Tungning is at peace with Manila and… | Choices |
| --- | --- | --- |
| **Manila merchants need warehouses** | Relations are at least +20 and Taiwan has a trade center | **Fit out bonded warehouses:** Spend 2% of the gold reserve cap for +15% trade advantage in Taiwan for one year. **Auction the leases:** Collect 2% of the cap up front; the Maritime Houses lose 2 approval for one year after being denied the concession they asked for. |
| **Two ports ask for the same rice** | Manila is fighting another war or turmoil in its Manila state is at least 15% | Both options spend 2% of the gold reserve cap on the cargo. **Honor Manila’s order:** Gain 10 relations and remove radicals equal to 5% of Pops in Manila’s state. This eases a crisis Tungning might otherwise benefit from. **Buy it for Taiwan:** Give Taiwan’s lower strata +1 standard of living for six months; lose 5 relations for taking a shipment Manila was counting on. |
| **The sisters ask for the old quarantine station** | Tungning is Catholic and the Devout are the Catholic Missions | **Grant the site for a free hospital:** Reduce mortality in Taiwan by 10% for two years and give the Catholic Missions +2 approval for one year. **Reserve the site for a public works yard:** Gain +10% construction efficiency in Taiwan for two years and give the Catholic Missions −2 approval for one year. |

Cash options require enough gold reserves at response. Show the amount and disable any option Tungning cannot afford. Resolved event effects run for their stated terms even if the journal closes. End a Taiwan modifier early if Tungning loses the recipient state. Events cannot sign an agreement, choose a subject type, grant territory, or start a play.

## Establish Tungning rule

- **Submission:** Become the direct overlord of the Philippines while it still owns Manila. Ratify the charter, use another legal agreement where available, or enforce a native subjugation demand. Make Tributary and Make Protectorate depend on vanilla rank and recognition rules. Keep the Philippine tag and its vanilla content.
- **Conquest:** When the window starts, record provinces `PHI` owns in Luzon and the Visayas. Tungning must directly own Manila, more than half of the recorded set, and Cebu (`p:xD2CA4A`) if that city was in the set. Require a territorial goal enforced in a qualifying play against the Philippines. Occupation and land taken from an unrelated country cannot satisfy the route by themselves.
- **Qualifying play:** Tungning must initiate it against independent `PHI` during the window and demand Philippine submission or territory. Record enforcement before checking ownership, so a goal that extinguishes `PHI` can still count for conquest.
- **Deadline:** Cancel pending offers and petitions at expiry. Wait for a qualifying play that is already underway, and record its identity. No new play extends the window.

## Outcomes, AI, and static checks

- **Resolution:** Check success before suspension or expiry, including conquest that extinguishes `PHI`. Record whether submission came through an agreement or an enforced goal, or whether Tungning took direct rule. Apply the [Manila aftermath](outcome-modifiers.md#manila) from that result. If the clock runs out during suspension or the tracked deadline conflict ends unsuccessfully, close without a territorial penalty. Visibility before the window starts is not an expired opportunity.
- **Later rule:** Philippine holdings still under Tungning become eligible for [the Southern Compact](07-reunification-of-china.md#the-home-and-southern-settlements) once this journal closes.
- **AI:** Seek a trade agreement and offer the charter when relations make consent plausible. Manila should weigh its need for protection against losing independence; a reliable foreign protector makes refusal more likely. Consider a play when Manila is distracted, Tungning can field land and naval forces, and likely third-party intervention is manageable. A governing southern-expedition leader favors that route; mainland-first leadership favors keeping the ships at hand. Fund the expedition only if a landing is needed and the fleet and troops are ready. Weigh the petitions against current reserves, Taiwan’s trade and construction, and whether preserving goodwill in Manila is useful. Other journals do not gate Manila.
- **Display:** Show the deadline, progress toward both routes, the charter’s market concession, the expedition’s cash cost and remaining term, and concrete blockers such as rank, missing interests, subject restrictions, or a third-party overlord.
- **Verify:** Spanish rule, independent Manila, a third-party handover, renewed Spanish authority, accepted and refused charters, and loss of eligibility while an offer is pending. Trace a funded expedition into a deadline hold and into a second war. Check cash and ownership changes before petition responses, and conquest that extinguishes `PHI`.
- Vanilla: `common/history/diplomacy/00_subject_relationships.txt` (Spanish colony), `common/journal_entries/06_philippines_je.txt` (Philippine independence), `map_data/state_regions/12_indonesia.txt` (Luzon and the Visayas), `common/diplomatic_plays/00_diplomatic_plays.txt` (native plays), and `common/diplomatic_actions/36_subjects_grant_own_market.txt` (market concession). See the [Strait Accord effect](../../common/scripted_effects/fh_strait_accord.txt) for an existing subject pact paired with a market grant.
