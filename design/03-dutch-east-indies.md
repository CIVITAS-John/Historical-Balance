# The Southern Passage

Dutch merchants and naval stations can cut off the routes that make Tungning’s southern holdings worth keeping. This journal asks whether the kingdom can defend those routes before the local courts conclude that its protection is a paper promise.

## Entry and stakes

Start `fh_je_southern_passage` after the day-eight diplomacy retry if a Dutch rival and at least one opening holding exist. Snapshot only the Sintang, Selangor, and Bulungan tributaries that the setup granted and that are still direct subjects, and only the original Lanfang parcels the setup acquired: `x1C7417`, `x2A3D46`, `xE02CB6`. Keep their identities fixed if the map changes. If the Dutch East Indies (`DEI`) disappears, substitute the Netherlands only if it now holds land in West Java. If neither remains a regional rival, close the entry without concessions or a victory reward.

## Pressure and challenge

Start **Dutch pressure** at **10/100**. It rises **2 per month**, plus **1** if the Dutch side has higher effective projection and **1** if Tungning is in default. The Dutch comparison uses `DEI`’s naval power projection, with a floor of one quarter of the Netherlands’ projection if it is the overlord. If the Netherlands rules directly, use one quarter of its projection. This represents the force the Netherlands can spare locally. Also record Tungning’s opening projection. Notify at 50 and 75. At 100, concede unless a success condition or the active-play hold applies.

| Action | Effect |
| --- | --- |
| **Fund the Convoys** | Spend 5% of the gold reserve cap from existing cash for −12 pressure; available every 12 months. A five-year deadline still applies. |
| **Challenge the Dutch** | Requires an active interest in Indonesia, no default, and naval power projection at least the Dutch comparison value and at least 120% of Tungning’s recorded opening projection. Worsens relations with the local Dutch rival by 20, once. Opens the option of proving the challenge without war. |
| **Demonstrate control of the passage** | After declaring the challenge, maintain its interest, projection, and fiscal requirements for 12 consecutive monthly checks. Losing an opening holding after the challenge starts resets the streak; it does not prevent defending the rest. At least one holding must survive. |
| **Defeat a Dutch challenge** | A native enforced war goal against the tracked rival (or its Dutch overlord) qualifies if Tungning pressed it and it transfers a state held by that rival in Indonesia or compels them to recognize Tungning’s independence, when the goal is legal. A victory or white peace unrelated to these interests does not count. This route can succeed without using the button. |

At 100 pressure or the five-year deadline, defer concessions only if Tungning and the tracked Dutch side are currently opponents in a diplomatic play or war. Record that specific play and reassess when it ends; a qualifying enforced goal can still win. No new play, challenge, or convoy purchase extends the hold. The deadline otherwise resolves the journal even if pressure is below 100. Warn that buying time does not by itself secure the routes.

## Outcomes

**Secure the passage.** Keep the remaining holdings, gain +10 prestige and +5% trade capacity in Tungning’s West Borneo state, if still held, for five years. No free land, subjects, or future guarantee.

**Concede the passage.** Release only the tracked courts that are still direct Tungning tributaries. Do not make them Dutch subjects by script. Cede the tracked Lanfang parcels still owned by Tungning to the qualifying Dutch rival, using individual transfers. If the rival ceases to qualify before execution, cancel the deadline and close without forfeiture. Territory already lost is never moved, another power’s subjects are untouched, and neighboring West Borneo parcels are never included. If every tracked holding is already lost before this point, close as already lost with no further penalty.

Qing tributary status by itself is not a loss. It can restrict war choices under vanilla rules; the naval demonstration remains available. The AI protects the position when it can afford the challenge and favors convoy funds only when they can buy enough time for an achievable demonstration. Verify no starting holdings, replacement of the DEI by direct Dutch rule, a partial transfer, changed overlord, and a defeat of the relevant opponent versus an unrelated war.

Existing setup: `common/scripted_effects/fh_tungning_diplomacy.txt:70–105` and `common/scripted_effects/fh_tungning_setup.txt:98–121`. Vanilla references: `common/journal_entries/02_brazil_navy.txt:44–77` (naval projection), `common/on_actions/00_code_on_actions.txt:3699–3707` (enforced war goals), and `common/scripted_effects/00_chris_scripted_effects.txt:314–330` (individual province cession).
