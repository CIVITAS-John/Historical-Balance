# The Return to the Mainland

**Proposed design.** This journal is about establishing a mainland administration. Directly own all land except treaty-port enclaves in **one** of Fujian, Guangdong, or Zhejiang, clear any enemy occupation, and use **Incorporate State**. At **50% incorporation**, the foothold registers automatically. [The Reunification of China](07-reunification-of-china.md#opening-and-progress) opens separately when Tungning directly owns **all three** coastal regions.

## Opening

- **Reassert:** The journal opens even without a foothold, including after reassertion at the [Taiping fork](08-taiping-rebellion.md#the-last-chance).
- **Gain a foothold:** Direct ownership under the [mainland claim rules](01-mainland-claim.md#mainland-foothold) also opens the journal. If the claim is unsettled, first record reassertion. If the Taiping choice is already pending, record the foothold but wait for the court to reassert.
- **After renunciation:** A foothold can still open the journal without starting mobilization, reviving Ming restoration, or altering a Qing treaty. Permanent abandonment at the Taiping fork closes this route.

## Mobilization after reassertion

Mobilization lasts up to **three years**. Army and fleet formations regain Organization **25% faster**, but contributions to the Investment Pool fall **50%**, leaving less money for private construction. For the same period, the Ming Estates gain **+5 Approval** and the Maritime Houses lose **5 Approval**. The Army and Fleet gain **+5** under a mainland-first leader, lose **2** under a southern-expedition leader, and otherwise see no change. Use the officer stance when mobilization starts.

- **When it ends:** Mobilization ends after three years or when Tungning’s first war against Qing or its successor central government ends, whichever comes first. Count wars already underway and wars whose peace settlement triggers reassertion. If Tungning reasserts at the Taiping fork during the rebellion, mobilization also ends if the rebellion ends first. Reasserting after the rebellion ends starts ordinary mobilization.
- **A War Never Fought:** If Tungning neither fights a qualifying war nor delivers aid under its Taiping pact during fork mobilization, it loses **5 Base Legitimacy for one year**. The Army and Fleet also lose **3 Approval for that year** if their leader is mainland-first when mobilization ends. An ongoing war counts; a backdown or a pact without delivery does not.
- **The Failed Crossing:** Losing the first tracked war costs **5 Base Legitimacy for one year**, even if mobilization ended while the war was still going.
- **Constitutional debate:** The [debate](05-constitutional-settlement.md#opening) opens when mobilization ends, regardless of whether Tungning fought. The penalty does not delay it.

## Decision: Press the Mainland Claims

After reasserting, use **Press the Mainland Claims** to preview demands against **one** eligible government at a time. Show the target and each outstanding claim it holds in Fujian, Guangdong, and Zhejiang. Only Qing or eligible mainland successors can be targeted. While the [Taiping pact](08-taiping-rebellion.md#collect-the-promises) is in force, use its settlement instead of this play against Taiping.

Confirm the preview to start a normal diplomatic play. The preset **Return State** demands cost **no Infamy**; additional demands follow the ordinary rules. Exclude treaty ports and holdings of unrelated foreign powers. Show blocked targets and why, then recheck ownership, claims, and diplomatic restrictions on confirmation. The decision stays available during reunification for any legal coastal claim.

## Consolidate the foothold

Only a region where Tungning directly owns **all ordinary land** and none of that land is under enemy occupation can fill the bar. Actual treaty ports do not have to be recovered. For example, Macao can remain foreign while it is a treaty port. If it becomes ordinary foreign land again, it counts as missing. Owning only a treaty port or relying on a subject to hold part of a region is not enough.

The bar tracks the eligible region with the most **incorporation progress**. An incorporated state counts as complete. Show the leader and what is blocking each of the three regions: missing land and its owners, occupation, or an unstarted project. Point to where to start a project or use a decree. Losing an eligible region can lower the bar, but the journal stays open and does not reset incorporation projects.

At **50%**, registration is automatic. If the **Port and Village Registers** are active, their extra conscription ends permanently and their **+10 Acceptance in homelands** remains. Registration grants no land, instant incorporation, timed bonus, or radical change. Losing the foothold later does not undo registration. The coastal recovery play remains available when legal.

## Mainland integration

Use ordinary **Incorporate State** projects at their normal Bureaucracy cost. Projects run slower on directly held ordinary land throughout the [mainland core](07-reunification-of-china.md#opening-and-progress), however acquired. This also applies to partial holdings that cannot register as a foothold. Taiwan, southern holdings, treaty ports, and subject land use ordinary rules.

- **Staff local Government Administration.** Offices speed up the project only when people actually work in them. Two half-staffed levels count as one. Inherited Qing offices help just as much as new offices.
- **Lower actual Turmoil.** Unrest slows incorporation even if other modifiers offset its usual penalties. Enemy occupation or at least 75% Turmoil usually cuts incorporation to one-tenth of normal speed. An occupied foothold cannot register.
- **Check the current rate.** Update it monthly and show why it changed. The foothold journal reads the same incorporation progress as the state panel.

Integration follows founding Tungning through a change of tag and continues after both journals end. A pending Taiping choice blocks special decrees and journal completion but leaves the slowdown in place. Permanent abandonment restores ordinary incorporation speed.

### State decrees

Set these policies in the usual state decree interface. Each uses **100 base Authority**, adjusted by Power Rank, while assigned. Each state can run one of these three policies at a time; remove the old one to switch. A project can progress without any decree. Preview the change to incorporation speed using the state’s current staffing and Turmoil.

| Decree | What it does in this state | What you give up |
| --- | --- | --- |
| **Keep the County Magistrates** | Incorporation moves faster even with few staffed offices. Active political movements create **25% fewer new radicals**. | Buildings progress more slowly in this state: **−10% State Construction Efficiency**. |
| **Send Taiwan Commissioners** | Incorporation moves faster for each staffed level of Government Administration. This works best where offices are well staffed. | Active political movements create **20% more new radicals**. |
| **Open Public Relief Offices** | Removes a small number of existing radicals each month while the state is unoccupied and has at least **25% Turmoil**. Less unrest can speed up incorporation later. | No direct bonus to incorporation speed. Below 25% Turmoil or under occupation, the Authority buys no monthly relief. |

For example, with **eight staffed levels and 20% Turmoil**, the state incorporates at **54% of normal speed** before other modifiers. Magistrates raise it to about **65%** and commissioners to **66%**. Relief changes neither the speed nor the number of radicals at 20% Turmoil. With no decree, a project that would normally take two years reaches the foothold milestone in about **22 months** and finishes in about **44 months**, if conditions stay the same.

The weekly decree check removes the policy once the state finishes incorporating, changes owners, or otherwise loses eligibility. A decree can stay assigned during occupation; the occupied speed penalty takes over at the next refresh, and relief does not run. Treaties and spontaneous coastal migration keep their own rules.

## Implementation and static checks

**Incorporation rate.** Count staffed Administration as building level times occupancy (capped at 10 staffed levels). Before vanilla modifiers, the rate is `(0.40 + 0.04 × staffed levels + decree bonus) × turmoil factor` of normal speed. The magistrate bonus is `0.15`; the commissioner bonus is `0.02 × staffed levels`. Relief adds no speed and uses `−0.005` as the initial value for the native monthly radical removal effect. Use a **−125 percentage point** speed modifier during occupation or at least 75% Turmoil; ordinary vanilla bonuses generally leave the engine’s 10% floor in effect.

| Actual Turmoil | Rate factor | Speed with eight staffed levels, no decree |
| --- | ---: | ---: |
| Below 10% | 1.00 | 72% of normal |
| 10% to under 25% | 0.75 | 54% of normal |
| 25% to under 50% | 0.45 | 32% of normal |
| 50% to under 75% | 0.20 | 14% of normal |
| 75% and above, or occupied | Use the severe speed penalty | Typically 10% of normal |

**Scripts.**

1. Add shared state eligibility (`fh_mainland_integration_state`), rate values, and the three definitions in `common/decrees/`. Reuse the recorded founding-country scope and [staffed levels value](../../common/script_values/fh_return_to_mainland.txt). Gate the decrees on the founder, campaign, and state; use `has_decree` to exclude the other two policies. Use a single namespaced `state_incorporation_speed_mult` modifier with base `−1`, scaled by `1 − rate` (or `1.25` for the severe penalty). Replace it on an appended monthly country pulse with a 35-day expiry. Initialize or clear it at state creation and owner change, remove it on incorporation, and recheck live eligibility before applying decree effects.
2. For `fh_je_mainland_foothold`, replace the current [three-check readiness streak](../../common/journal_entries/fh_return_to_mainland.txt) and [manual registration event](../../events/fh_mainland_registration.txt) with automatic registration. Keep the existing claim and ownership checks for opening. Use live ownership, occupation, and native `incorporation_progress` comparisons for completion. Share the direct ownership rule with reunification, but keep the registration flag and incorporation threshold out of its opening check. For display only, break ties in Fujian, Guangdong, Zhejiang order. Use native journal goal display (`current_value` and `goal_add_value` calculated to reach the fixed target). If exact numeric access is unavailable, round down in 10-point steps using the same trigger and leave exact progress in the state panel.
3. Preserve `fh_return_to_mainland_completed` and the existing levy retirement effect. Clear legacy pending registrations and readiness streaks without repeating an outcome or guessing which state an older save registered. Show the levy bonus the player is actually losing: the [current amendment](../../common/amendments/fh_law_amendments.txt#L62) grants +50% Conscription Rate; older localization and the README still say +25%. Align the recap with the active rule.
4. During mobilization, weight AI construction toward barracks and military supplies. Use **Press the Mainland Claims** only with at least 10 regular battalions, no default, a manageable opposing coalition, and either a target at war elsewhere or a target state with at least 25% Turmoil. For decrees, prioritize the coast and both national seats. Favor relief in severe unrest and remove it below 25%; favor commissioners in calm states with at least eight staffed levels and magistrates elsewhere when their rate gain matters.

**Static verification.**

- Check zero, fractional, capped, and inherited staffed levels, each Turmoil threshold, and each decree. Check switches, the pending Taiping choice, permanent abandonment, tag changes, and a victorious revolution. Verify that effects never stack or pass to a separate successor.
- Trace full and partial ownership, Macao as a treaty port or ordinary foreign land, treaty-port-only and subject holdings, occupation, recapture, state splits and merges, and incorporation completion. Check simultaneous acquisitions, automatic registration of just one region, loss and recovery, and old saves and reloads. The completed entry cannot repeat, and the levies stay off.
- Register one coast with the other two missing: reunification stays closed. Acquire all three coasts before starting incorporation: reunification opens and the foothold journal stays active.
- Trace reassertion, final renunciation, and a pending Qing offer. Check an early Qing war end, war lasting beyond expiry, backdown, defeat, a peace transfer that forces reassertion, and delivered versus unfulfilled Taiping aid. The no-war penalty only applies when Tungning did not follow through; the constitutional debate opens once.
- Check the claims preview with no eligible target, split ownership, a truce, and changed ownership before confirmation. Verify that only the preset demands are exempt from Infamy.
- Use standalone Tiger and `git diff --check` after scripting. Vanilla references: `common/decrees/00_decree.txt`, `common/journal_entries/06_morocco_lands_of_anarchy.txt`, `common/on_actions/00_code_on_actions.txt`, `map_data/state_regions/11_east_asia.txt`, and `common/treaty_articles/14_treaty_port.txt`. See the Balkan War button and play in `common/scripted_buttons/00_balkan_wars_buttons.txt` and `common/diplomatic_plays/00_diplomatic_plays.txt`.
- The Algerian Departments use native incorporation overseas (`common/journal_entries/01_algeria.txt`). Leave the playcheck to the user: verify Tungning can start from a single coastal foothold and its AI starts homeland projects. If the native rules block these projects, revisit the clock before adding a bypass. Keep global incorporation, AI, and migration rules unchanged.
