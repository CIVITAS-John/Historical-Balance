# The Southern Passage

Dutch merchants and naval stations threaten Tungning’s route to West Borneo and its southern tributaries. Tungning can buy time for its fleet or force the Dutch to yield in a diplomatic play.

The Maritime Houses want to protect their southern concessions and win new outlets. They prefer funded escorts and a naval demonstration that keeps cargo moving. Southern-expedition officers want the fleet to contest the Dutch openly; mainland-first officers object to committing ships needed across the strait.

## Opening

- **Entry:** `fh_je_southern_passage`. Open after the day-eight diplomacy retry if Tungning still holds at least one of the grants below and there is a Dutch rival.
- **Holdings:** Record only grants made by the opening setup that Tungning still holds: Sintang, Selangor, and Bulungan as direct tributaries, and the Lanfang parcels `x1C7417`, `x2A3D46`, and `xE02CB6`. Keep that list fixed.
- **Rival:** Track the Dutch East Indies (`DEI`). If it ceases to exist, switch to the Netherlands only if it owns land in West Java. If neither qualifies, close without concessions or a victory reward.
- **Opening effect:** Dutch competition gives Tungning’s West Borneo state **−10% trade advantage** while the journal is open and Tungning still holds a tracked Lanfang parcel. Remove the penalty when the journal closes or the state no longer qualifies.

## Dutch pressure

Start at **10/100** and warn at **50** and **75**. Apply monthly changes together and keep pressure between 0 and 100.

| Monthly change | Condition |
| --- | --- |
| +1 | Ongoing Dutch pressure |
| +1 | Effective Dutch naval projection exceeds Tungning’s |
| +1 | Tungning is in default or uses at least 75% of its credit |
| +1 | The tracked rival embargoes Tungning |
| −1 | Relations with the tracked rival are at least +20 |
| −1 | The rival or its Dutch overlord is fighting in another war; count this once |
| −1 | The Tungning trade center at West Borneo is higher than any of Dutch East Indies' |
| −1 | Tungning has a defense pact is guaranteed independence by Britain or East India Company |

Use the DEI’s naval power projection, or 25% of the Netherlands’ if that is higher and the Netherlands is its overlord. When the Netherlands is the rival directly, use 25% of its projection. Record Tungning’s opening projection for the challenge.

At **100 pressure** or the **fifth anniversary**, check for success before concessions. Reaching zero buys breathing room. The deadline still applies.

## Actions

- **Policy Challenge:** <!-- -12 pressure with 12mo cooldown. -100% export tariff, +2 maritime approval for 12 months -->
- **Military Challenge:** Requires an active interest in Indonesia, no default, and naval projection at least as high as the Dutch comparison and at least 120% of Tungning’s opening projection. Once per journal, reduce relations with the rival by 20 and start the naval demonstration. For one year, give the Maritime Houses −2 approval for risking trade and the Army and Fleet +2 under a southern-expedition leader, −2 under a mainland-first leader, or zero under a neutral leader. During the demonstration, raise naval goods costs by 25%.

## Events

Each quarter, roll a 10% chance to draw one eligible event. Start a shared 12-month event cooldown on draw. Ignore unanswered events and any response once a conflict hold begins or the journal closes.

| Event | Eligible while | Choices |
| --- | --- | --- |
| Merchants ask for escorts | Tungning still owns a tracked Lanfang parcel | Escort the ships (−5 pressure, +5% military goods costs) or leave the merchants to arrange their own passage (+5 pressure, +5% trade advantage in Tungning’s West Borneo state). |
| Dutch fleet called away | The rival or its Dutch overlord is fighting in another war | Use the opening (−5 pressure, +5% military goods costs) or keep ships on their usual routes (+5 pressure, +2 Maritime Houses approval). |

Event modifiers last six months. Recheck eligibility when the event is answered.

## Ways to secure the passage

- **Naval demonstration:** After the challenge, meet its interest, projection, and default checks at 24 consecutive monthly checks. A lost opening holding resets the streak. At least one holding must survive.
- **Enforced goal:** Tungning must enforce a native goal that wins a state held by the tracked rival, or humiliation, in Indonesia. The challenge is optional. White peace and victories over unrelated targets do not count.
- **Conflict at the deadline:** If Tungning and the tracked Dutch side are already opponents in a play or war when concessions would fall due, wait for that specific conflict. During the hold, only a qualifying enforced goal can win. Stop pressure changes and the demonstration, and suspend actions. No later play extends the hold.

## Outcomes

- **Secure:** Keep the remaining holdings and gain +10 prestige for five years. Tungning’s West Borneo state gains +5% trade advantage for five years if still held. Record the grants actually kept at victory for the [Zheng mandate](05-constitutional-settlement.md#zheng-dynasty); it checks current ownership or direct overlordship afterward.
- **Concede:** Recheck the rival and holdings. Transfer SEA holdings, tributaries, vassals to DEI. Transfer only recorded parcels Tungning still owns to the qualifying rival.
- **Close without concessions:** If Tungning loses all opening holdings, or no Dutch rival still qualifies, close without further penalties or rewards.

Surviving holdings become eligible for [the Southern Compact](07-reunification-of-china.md#the-home-and-southern-settlements) once this dispute ends. The compact does not revisit concessions or return lost holdings.

## AI and static checks

- Prioritize building enough naval strength to challenge. Fund convoys when they can buy enough time for a realistic demonstration. Challenge when the fleet can sustain it and the treasury can absorb the cost.
- Favor a legal territorial play when the Dutch side is busy elsewhere and Tungning can contest the likely opponents. A governing southern-expedition leader increases the AI’s preference for a challenge or play; a mainland-first leader favors convoys if mobilizing across the strait. Keep normal war costs and eligibility. Becoming Qing’s tributary may limit the war route; it does not trigger concessions or block the demonstration.
- Trace changes in pressure and rival, partial loss, loss of all holdings, a tributary changing overlord, and a conflict continuing past the deadline. Check that only an enforced qualifying goal wins.
- Setup: `common/scripted_effects/fh_tungning_diplomacy.txt` and `common/scripted_effects/fh_tungning_setup.txt`. Vanilla: `common/journal_entries/02_brazil_navy.txt` (projection), `common/on_actions/00_code_on_actions.txt` (enforced goals), and `common/scripted_effects/00_chris_scripted_effects.txt` (province transfers).
