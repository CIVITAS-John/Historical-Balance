# The Southern Passage

Dutch merchants and naval stations threaten Tungning’s southern routes. If the kingdom cannot protect them, it may lose the holdings the routes serve.

## Opening and holdings

- **Entry:** `fh_je_southern_passage`.
- **Requires:** After the day-eight diplomacy retry, a Dutch rival and at least one opening holding.
- **Tributaries:** Record only Sintang, Selangor, and Bulungan that the setup granted and that remain direct Tungning subjects.
- **Parcels:** Record only the original Lanfang parcels that the setup acquired: `x1C7417`, `x2A3D46`, and `xE02CB6`.
- **Rival:** Track the Dutch East Indies (`DEI`). If it disappears, substitute the Netherlands only if it now owns land in West Java.
- **Tracking:** Record which holdings setup actually granted, then keep that list fixed. If neither Dutch country qualifies, close without concessions or a victory reward.

## Dutch pressure

- **Starting pressure:** 10/100. Notify the player at 50 and 75.
- **Monthly drift:** +2 normally, +1 if the Dutch side has higher effective naval projection, and +1 if Tungning is in default.
- **Dutch projection:** Use the DEI’s naval power projection. If the Netherlands is its overlord, use the higher of the DEI’s projection and 25% of the Netherlands’ projection. If the Netherlands is the rival directly, use 25% of its projection.
- **Tungning projection:** Record its opening naval power projection for the challenge.
- **Deadline:** At 100 pressure or the fifth anniversary, concede unless a success condition or the active conflict hold applies. The deadline still applies below 100.

## Actions

- **Fund the Convoys**
  - **Requires:** At least 5% of the gold reserve cap in cash, and no active cooldown.
  - **Cost:** Spend 5% of the gold reserve cap from cash.
  - **Effects:** Reduce pressure by 12 and start a 12-month cooldown. The deadline stays in place. Tell the player this buys time without securing the passage.
- **Challenge the Dutch**
  - **Requires:** An active interest in Indonesia, no default, and naval projection at least as high as the Dutch comparison and at least 120% of Tungning’s opening projection.
  - **Effects:** Reduce relations with the local rival by 20 once and unlock the naval demonstration.

## Ways to secure the passage

- **Naval demonstration**
  - After declaring the challenge, meet its interest, projection, and fiscal requirements at 12 consecutive monthly checks.
  - Losing an opening holding after the challenge begins resets the streak. At least one holding must survive.
- **Enforced war goal**
  - Tungning must press and enforce a native war goal against the tracked rival or its Dutch overlord.
  - The goal must transfer a state held by that rival in Indonesia or compel recognition of Tungning’s independence, where the goal is legal.
  - The challenge button is optional for this route. An unrelated victory or white peace does not count.
- **Active conflict hold**
  - At the deadline or 100 pressure, defer concessions only if Tungning and the tracked Dutch side are already opponents in a diplomatic play or war.
  - Record that specific play and reassess when it ends. A qualifying enforced goal can still win.
  - A new play, challenge, or convoy purchase cannot extend the hold.

## Outcomes

### Secure the passage

- Keep the remaining holdings.
- Gain +10 prestige for five years.
- Gain +5% trade capacity in Tungning’s West Borneo state for five years, if still held.
- Grant no new territory, subjects, or guarantees.

### Concede the passage

- If all tracked holdings are already gone, close as already lost with no additional penalty.
- Recheck the Dutch rival before applying concessions. If it no longer qualifies, close without forfeiture.
- Release only tracked courts that are still direct Tungning tributaries. Do not make them Dutch subjects by script.
- Transfer only tracked Lanfang parcels that Tungning still owns to the qualifying Dutch rival, one at a time.

## AI and static checks

- Qing tributary status does not trigger loss. Native subject rules may limit war choices; the naval demonstration remains available.
- The AI challenges when it can afford to. It funds convoys only when they can buy enough time for an achievable demonstration.
- Verify no opening holdings, a switch from the DEI to direct Dutch rule, partial cession, a subject that has changed overlord, and an enforced goal versus an unrelated victory.
- Setup references: `common/scripted_effects/fh_tungning_diplomacy.txt` and `common/scripted_effects/fh_tungning_setup.txt`.
- Vanilla references: `common/journal_entries/02_brazil_navy.txt` (naval projection), `common/on_actions/00_code_on_actions.txt` (enforced war goals), and `common/scripted_effects/00_chris_scripted_effects.txt` (individual province cession).
