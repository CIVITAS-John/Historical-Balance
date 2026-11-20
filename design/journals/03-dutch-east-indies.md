# The Southern Passage

Dutch merchants and naval stations threaten Tungning’s route to West Borneo and its southern tributaries. The Maritime Houses want cheap passage and open markets. Southern-expedition officers want the squadron to break Dutch pressure; mainland-first officers want those ships available across the strait. The court can buy time for the fleet, show it can keep the route open, or win a demand through ordinary diplomacy and war.

The entry runs alongside the mainland claim and the court faith debate. A victory can strengthen the Zheng mandate if Tungning keeps a grant it defended. A setback costs prestige and can cost the disputed Borneo parcels.

## Opening

- **Entry:** Start `fh_je_southern_passage` once, after the day-eight diplomacy retry, if the founding country still holds at least one tracked grant and has a qualifying rival. Keep the entry through a change of tag on the founding country; do not recreate it for a successor or reopen it after closure.
- **Opening grants:** Record successful setup grants when they are made, then keep only those still held after the retry. Track Sintang (`STG`), Selangor (`SEL`), and Bulungan (`BLG`) and the Lanfang parcels `x1C7417`, `x2A3D46`, and `xE02CB6`. Freeze that list at opening. A court counts while it survives under Tungning’s direct overlordship; a parcel counts while Tungning directly owns it. The separate Sambas and Pontianak pacts and later acquisitions do not enter the list.
- **Rival:** Record the living Dutch East Indies (`DEI`) if available. Otherwise use the Netherlands (`NET`) if it directly owns ordinary land in West Java. If the DEI disappears mid-entry, make the same fallback once and reset the demonstration streak. Keep Tungning’s original fleet baseline and the original deadline.
- **Opening effect:** Apply **−10% trade advantage** to Tungning’s West Borneo state while the journal is open and the state contains a tracked Lanfang parcel. This includes a conflict hold. Remove the effect on closure or loss of eligibility. It may return if Tungning regains a tracked parcel while the entry is still open.

## Dutch pressure

Start at **10/100**. Warn once at **50** and **75**. Sum the monthly factors before clamping the bar to 0–100. Reaching zero buys time; it does not settle the dispute.

| Monthly change | Condition |
| --- | --- |
| +1 | Ongoing Dutch pressure |
| +1 | Effective Dutch naval projection exceeds Tungning’s |
| +1 | Tungning is in default or uses at least 75% of its credit |
| +1 | The recorded rival embargoes Tungning |
| −1 | Relations with the rival are at least +20 |
| −1 | The rival or its direct Dutch overlord is fighting a war that does not involve Tungning; count this once |
| −1 | Tungning still holds a tracked Lanfang parcel and its West Borneo trade center is larger than the rival’s largest trade center in Indonesia |
| −1 | Great Britain (`GBR`) or the East India Company (`BIC`) has an active defensive pact with Tungning or guarantees its independence; count this once |

Use nominal trade center levels. Tungning needs a trade center above level zero; a rival with no trade center in Indonesia has level zero for the comparison. For the fleet, use the greater of the DEI’s naval projection and **25%** of the Netherlands’ while the Netherlands is its direct overlord. Use **25%** of Dutch projection if the Netherlands is the rival itself. Save Tungning’s projection at opening.

At **100 pressure** or on the **fifth anniversary**, check for success before concessions. If a scheduled monthly check falls on the anniversary, run it once before resolving expiry. Show the deadline, each monthly factor, the fleet comparison, and the current demonstration streak.

## Court actions

- **Tariff Challenge:** Reduce pressure by **12** and give the Maritime Houses **+2 approval for one year**. For the same year, reduce the maximum export tariff by **10 percentage points** (`state_tariff_export_add = -0.10`). This offsets the Anping Trade Charters’ full opening rate and gives partial relief under vanilla Mercantilism or Protectionism. Require one of those laws and a market whose tariff policy Tungning controls. The revenue cost depends on the duties it actually charges. End the relief if either condition is lost, a conflict hold begins, or the entry closes. Leave import duties, subventions, and per-good settings unchanged. The **12-month cooldown** does not extend the deadline.
- **Military Challenge:** Once per entry, require a fully active interest in Indonesia, no default, and naval projection at least equal to both the effective Dutch fleet and **120%** of Tungning’s opening projection. Lose **20 relations** with the rival and start the demonstration. Give the Maritime Houses **−2 approval** and the Army and Fleet **+2** under a southern-expedition leader, **−2** under a mainland-first leader, or zero otherwise, for **one year**. While the demonstration runs, pay **+25% naval goods costs**. The increase lasts through setbacks; it leaves army goods and wages alone. A hold or closure ends the cost. Approval records the decision at the time and runs for its stated term.

Both actions require an active dispute. Show the full cost and any unmet requirement before committing.

## Events

Every third monthly pulse during the active dispute, roll a **10%** chance to draw one eligible event. On draw, start a shared **12-month cooldown** and allow **30 days** for a response. Dismissing a petition or letting it expire has no effect. Recheck its conditions and the recorded rival on response; a hold, closure, or rival switch cancels pending choices.

| Event | Eligible while | Choices |
| --- | --- | --- |
| **Merchants ask for escorts** | Tungning still owns a tracked Lanfang parcel | Fund escorts (**−5 pressure**, **+10% naval goods costs** for one year), or let merchants arrange their own passage (**+5 pressure**, **+10% trade advantage** in Tungning’s eligible West Borneo state for six months). |
| **The Dutch fleet is called away** | The rival or its direct Dutch overlord is fighting a war that does not involve Tungning | Send out the squadron (**−5 pressure**, **−5 relations** with the rival, **+10% naval goods costs** for one year), or keep ships on their usual routes (**+5 pressure**, **+2 Maritime Houses approval** for six months). |

Use Yang Jingyuan for the merchants if he is alive and still in Tungning; otherwise use an unnamed shipping delegate. Use a serving officer or an unnamed captain for the fleet report. Reuse one escort cost modifier so two escort choices cannot stack with each other. A paid escort can overlap the demonstration and ends at expiry or when the dispute closes. The local event modifier ends early if its state stops qualifying and does not return on recapture.

## Ways to secure the passage

- **Naval demonstration:** After the Military Challenge, meet the same interest, projection, and default requirements at **24 consecutive monthly checks** and retain at least one opening grant. A failed check or loss of a held grant resets the streak. The next passing monthly check can start a new streak with the holdings that remain. Recapture does not erase a reset. Check the demonstration before applying concessions on a shared tick.
- **Enforced goal:** Tungning must enforce a native goal that transfers ordinary state territory in Indonesia from the recorded rival to Tungning. **Humiliation** also counts in a direct play between Tungning and the rival if the rival held ordinary land in Indonesia when they became opponents. This gives the country-level demand a southern context and excludes humiliation added to another country’s dispute. A treaty port alone, occupation, a goal benefiting an ally, and white peace do not count. The challenge is optional.
- **Conflict hold:** If Tungning and the rival itself are already on opposing sides of a play or war when concessions fall due, save that exact play and rival. If there is more than one, use the earliest qualifying play. Freeze the pressure and the demonstration; suspend actions and cancel pending events. Only an enforced goal in the saved play can win during the hold. When it ends or is invalidated, resolve the dispute; a later play cannot extend it.

## Outcomes

Apply the matching [Southern Passage aftermath](outcome-modifiers.md#southern-passage) once. A hold allows only enforcement until the saved conflict ends. Then run the checks below without starting a new hold.

1. **Secure by enforced goal.** Read the irreversible enforcement before reacting to ownership or subject changes from the same settlement. Take the surviving-grant snapshot after those changes. A backdown or separate capitulation can qualify, even if it removes the last grant or the old rival.
2. **Lose all grants.** If no grant survives and there was no qualifying enforcement, close without ceding anything.
3. **Lose the rival.** If a grant survives, try the Dutch fallback before closing. Continue against a valid fallback if concessions are not yet due.
4. **Secure by demonstration.** Require a valid rival, a complete streak, and a surviving grant. Enforcement takes priority if both routes qualify together.
5. **Concede.** If pressure, the anniversary, or the end of the saved conflict calls for concessions, transfer only the tracked Lanfang parcels Tungning still owns to the current qualifying rival. Recheck each owner before transfer. The opening tributaries, other subjects, and unrelated territory keep their existing status. If only tributaries survive, apply the prestige and radical effects of concessions without transferring land.

On either victory, set the success flag and record just the opening grants Tungning still holds. The [Zheng mandate](05-constitutional-settlement.md#zheng-dynasty) checks whether Tungning currently keeps any of those grants; an enforced-goal victory without a surviving grant still gets its aftermath but gives no mandate progress. After closure, surviving holdings become eligible for the [Southern Compact](07-reunification-of-china.md#the-home-and-southern-settlements).

## Implementation order

1. **Opening and bar.** Record grant provenance in `common/scripted_effects/fh_tungning_setup.txt:128` and `common/scripted_effects/fh_tungning_diplomacy.txt:170`; start from the hidden retry in `events/fh_tungning_events.txt:89`. Use `fh_is_tungning_founder` (`common/scripted_triggers/fh_mainland_claim.txt:1`), nontransferable native journal outcomes, and one scripted bar with localized, phase-gated monthly factors (`common/scripted_progress_bars/fh_mainland_claim.txt:1`). Schedule the guarded anniversary as journal 02 does (`common/scripted_effects/fh_court_faith.txt:2`). Do not infer opening grants for old saves from present ownership.
2. **Actions and events.** Add `fh_southern_passage` scripted buttons, triggers, modifiers, on-actions, events, and localization alongside the corresponding journal 01/02 files. Reconcile the current phase before any action or response; apply pressure through one effect that checks the endpoints. Reuse the Army and Fleet stance checks (`common/scripted_triggers/fh_mainland_court.txt:1`) and the event guards (`common/scripted_effects/fh_court_faith.txt:299`). Check grant losses on ownership and subject changes, with monthly reconciliation as a backstop. Use state owner and creation hooks to strip West Borneo effects from ineligible states.
3. **Conflict and settlement.** Save the rival and play scope while they are opponents. Use native goal hooks to read the precise goal type and target before transfers. Confirm permanent enforcement with vanilla `on_wargoal_enforced` (`common/on_actions/00_code_on_actions.txt:3736` in vanilla). Match temporarily executed goals by their exact scope when permanent enforcement is later confirmed. Use play end and backdown hooks to reconcile holds. Defer loss, fallback, and concessions while enforcement and transfers from the same settlement are pending, even if the wider war continues. Use one guarded resolution effect and vanilla `transfer_province` for the fixed parcels. Record the result before applying aftermath, clear the opening and preparation effects, and show the actual transfer and aftermath in the recap.
4. **Zheng mandate.** Before closing a victory, write `fh_southern_passage_secured` and only the applicable `fh_southern_passage_secured_{stg,sel,blg,x1c7417,x2a3d46,xe02cb6}` flags. The consumer already exists at `common/scripted_triggers/fh_constitutional_mandates.txt:137`. Keep the snapshot fixed after closure.
5. **AI.** Prefer tariff relief when it buys useful time and its revenue cost is manageable. Challenge only if the fleet clears both thresholds, at least 24 checks remain, and the treasury can sustain the cost. A governing southern-expedition leader favors the challenge and a viable native play; a mainland-first leader favors keeping ships available during mainland mobilization. Use local action weights and native war eligibility; leave journal 01’s mobilization strategy in control. Qing tributary status can limit a play; it does not end the journal or block a demonstration.

## Static checks and limits

- Use journal 01’s **±2 approval**, **+5% goods costs**, and **+10% local trade advantage** as the short-term benchmarks (`common/static_modifiers/fh_mainland_court.txt:1`). With its **−50% naval goods costs** still active, the demonstration alone moves the combined modifier to **−25%**, which raises the bill by half before other effects. Adding an escort takes the combined modifier to **−15%** while it lasts. Keep the existing aftermath targets: **+15 prestige and local +10% trade advantage for four years** for a demonstration; **+20 and local +15% for six years** for enforcement. Trace tariff relief under each eligible law, after a law or market change, and with no duties selected.
- Trace a failed setup grant, loss and recapture of one parcel, a court changing overlord, loss of all grants, the Dutch fallback, a stale event response, and a change of tag. Check that a foreign state inherits no local effect and that a lost aftermath companion cannot restart on recapture.
- Trace a successful 24th check at the deadline, a hold ending in white peace, a rival backdown, simultaneous enforcement and loss of the last grant or rival, a goal benefitting an ally, and an unrelated play started after the hold. Check the typed goal hooks and exact goal ID against the installed scripts and standalone checks. Temporary occupation cannot award victory unless the exact goal later becomes permanent.
- Trace partial and subject-only concessions, one award per closure across reloads, and the mandate check after losing a grant secured at victory. Run `git diff --check` and standalone Tiger after scripting. Follow [AGENTS.md](../../AGENTS.md) for static validation.

This plan leaves starting forces, other journal rules, existing treaty terms, and native diplomatic play rules unchanged.
