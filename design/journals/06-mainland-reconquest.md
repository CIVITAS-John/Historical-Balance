# The Return to the Mainland

The first task is to establish a government on the mainland that can survive the next war. Fujian, Guangdong, or Zhejiang can serve as that foothold. Holding one is enough to begin the larger campaign.

## Opening

- **Entry:** `fh_je_mainland_foothold`. Open on recorded reassertion, including through the [Taiping fork](08-taiping-rebellion.md#the-last-chance), or when Tungning first meets the [ownership rule](01-mainland-claim.md#mainland-foothold). If an unsettled claim resolves through ownership, record reassertion before opening this entry. While the Taiping fork awaits an answer, record any foothold gained but hold this entry closed until the court reasserts.
- **Existing settlement:** Ordinary renunciation does not sponsor a mainland campaign, but a later qualifying foothold can still open this entry without reviving Ming restoration, starting mobilization, or changing a Qing treaty. Permanent abandonment at the Taiping fork bars this entry entirely.
- **Display:** The progress bar lists what is holding up each of the three possible footholds, including outstanding ordinary land and its current owners. Losing land updates the bar; the journal stays open.

## Mobilization after reassertion

- **Starts:** Apply the three-year [reassertion package](01-mainland-claim.md#reassert-the-claim) once when the court chooses Reassert, including when a foothold forces that choice. During mobilization, give AI Tungning more weight for barracks and their military supplies.
- **Ends:** Remove the package after three years or at the end of the first war in which Tungning fights Qing or its successor central government, whichever comes first. Count a war already in progress at reassertion and a war whose peace settlement forces reassertion. If Tungning reasserts at the Taiping fork while the rebellion is active, also end mobilization when that rebellion ends; fighting or actually delivering pact aid counts as following through. Answering the fork after the rebellion ends starts ordinary mobilization.
- **No war:** If the package ends without qualifying action, fire **A War Never Fought** once: −5 base legitimacy for one year, and −3 Army and Fleet approval if its leader is mainland-first at expiry. A backdown or a signed but unfulfilled pact does not count; a war still active at expiry does.
- **Defeat:** If the first tracked war ends in defeat for Tungning, apply −5 base legitimacy for one year. This can still happen if the three-year mobilization expired during that war.
- **Next journal:** Open the [constitutional debate](05-constitutional-settlement.md#opening) when mobilization ends. The no-war event does not extend the wait.

## Decision: Press the Mainland Claims

- **Available after Reassert:** Target one eligible owner at a time and assemble Return State demands for its claimed ordinary holdings in Fujian, Guangdong, and Zhejiang. This can target Qing or an eligible mainland successor that actually holds the land. Skip territory already recovered, treaty-port enclaves, and ordinary holdings of unrelated foreign powers. Suspend the preset play against Taiping while the wartime pact is in force; use its settlement process.
- **Diplomacy:** Only the preset coastal demands carry no infamy. Use normal play and settlement phases; check truces, existing conflicts, subject restrictions, interests, and eligibility. Show the target and demands before confirmation and recalculate them if control changes. Keep this separate decision available during reunification for unresolved coastal claims.
- **AI:** Use the decision only with at least 10 regular battalions, no default, a manageable opposing coalition, and either the target already fighting another war or at least 25% turmoil in one of its eligible target states.

## Consolidate the foothold

The journal tracks whichever of Fujian, Guangdong, or Zhejiang is furthest along. A region contributes only while Tungning owns all its ordinary land and none of that land is occupied by an enemy. The bar reaches its goal at **50% native incorporation** in any one eligible region. A state that the game already considers incorporated counts as complete. Show which region leads, what is blocking progress, and where to start incorporation or issue a decree. Break ties in Fujian, Guangdong, Zhejiang order for display only.

At the goal, record registration automatically and once. This permanently repeals the Port and Village Levies amendment, ending its +25% conscription bonus, and opens [The Reunification of China](07-reunification-of-china.md#opening-and-progress). The Registers’ homeland acceptance bonus remains. The court does not grant instant incorporation, a timed registration bonus, or extra land. The bar can fall when eligibility is lost; it never erases native incorporation progress. If Tungning later loses all three footholds, the completed entry stays closed and reunification’s national actions wait for a qualifying foothold. Legal coastal recovery plays remain available, and the original claim still settles on ownership alone.

## Mainland integration

Taiwan’s civil service cannot take over the mainland in one sitting. Start projects with the normal **Incorporate State** action and pay the game’s bureaucracy costs. The same slower rate applies to every ordinary, directly held, unincorporated [mainland core state](07-reunification-of-china.md#opening-and-progress), including partial holdings, regardless of how it was acquired. Taiwan, southern holdings, treaty ports, and subject lands stay outside the system. It belongs to the founding Tungning country and continues after both journals finish. A pending Taiping fork suspends the special decrees and journal completion, but the default slowdown continues. Permanent abandonment returns incorporation to normal rules.

Each month, read actual **Turmoil** and staffed **Government Administration**. Count a half staffed level as half a level and cap the contribution at ten. The starting rate is `(0.40 + 0.04 × staffed levels + decree bonus) × turmoil factor` of unmodified incorporation speed. For occupation or at least 75% turmoil, use a **−125 percentage point** speed modifier instead, so normal vanilla bonuses generally leave the state at the engine’s 10% speed floor. Occupied states never count toward journal milestones. Other vanilla bonuses and costs still apply.

| Actual turmoil | Rate factor | Default speed with eight staffed levels, before other modifiers |
| --- | ---: | ---: |
| Below 10% | 1.00 | 72% |
| 10% to under 25% | 0.75 | 54% |
| 25% to under 50% | 0.45 | 32% |
| 50% to under 75% | 0.20 | 14% |
| 75% and above | Engine floor in typical conditions | 10% |

In an ordinarily two-year homeland state with eight staffed levels, 20% turmoil means roughly 22 months to the first foothold milestone and 44 months to full incorporation before other modifiers. This gives the court time to add offices, hire staff, and decide which states get its limited Authority. Inherited Qing offices help if they are staffed. Techniques that only hide the effects of turmoil do not raise the rate.

### State decrees

Choose a policy in the usual state decree interface. Each costs **100 base Authority**; only one of these three can run in a state, but different states can use different policies. Remove the current decree before switching. No decree is required to make progress.

| Decree | What the province gets | Tradeoff |
| --- | --- | --- |
| **Keep the County Magistrates** | Add `0.15` to the rate before the turmoil factor. Keep local offices and reduce new radicals from political movements by 25%. | −10% state construction efficiency while local offices retain control of public works. Useful even with few staffed offices. |
| **Send Taiwan Commissioners** | Add `0.02 × staffed levels` to the rate before the turmoil factor. Standardized accounts make well staffed offices faster. | +20% radicals from political movements. Best where staffing is high and resistance is low. |
| **Open Public Relief Offices** | While unoccupied and at or above 25% actual turmoil, remove a small amount of radicals each month (initial value `−0.005` in the native state effect). | No direct speed bonus. Spend Authority now to improve future progress and local conditions. |

Decrees become invalid on incorporation, ownership loss, or loss of campaign eligibility; the native weekly check removes any spent decree. Occupation blocks relief and applies the occupied speed penalty at the next refresh; a decree can stay assigned until the area is secure. The AI prioritizes the coast and the two national seats, favors relief in severe unrest and stops using it below 25%, prefers commissioners in calm states with at least eight staffed levels, and uses magistrates elsewhere when the rate gain matters. Existing treaty commitments and spontaneous coastal migration keep their own rules.

## Implementation and static checks

1. Add one shared state eligibility trigger (`fh_mainland_integration_state`), the rate values, and the three definitions in `common/decrees/`. Reuse [the existing staffed levels value](../../common/script_values/fh_return_to_mainland.txt). Record the founding country scope at setup so the policy survives a tag change and cannot pass to another country with a copied variable. Gate each decree on that country and campaign status; use `has_decree` in its state trigger to exclude the other two policies. Add one namespaced `state_incorporation_speed_mult` modifier with base `−1` and multiply it by `1 − rate` (or `1.25` for occupied or severely troubled states). Replace it from an appended monthly country pulse with a 35-day expiry; initialize or clear it on state owner change and creation, and remove it when incorporation finishes. Recheck live eligibility before applying decree effects. Vanilla references: `common/decrees/00_decree.txt`, `common/journal_entries/06_morocco_lands_of_anarchy.txt`, and `common/on_actions/00_code_on_actions.txt`.
2. Replace the [readiness streak](../../common/journal_entries/fh_return_to_mainland.txt) and [registration event](../../events/fh_mainland_registration.txt) with the read-only journal bar and an automatic outcome. Use native `incorporation_progress` comparisons for the actual goal. For display, use the native journal goal (`current_value` and `goal_add_value`, calculated to reach the fixed target); verify numeric access or round down using the same trigger at 10 point steps and leave exact progress in the native state panel. Preserve `fh_return_to_mainland_completed` and the call to `fh_remove_port_and_village_levies`. Clear old pending registrations and streak values without repeating a reward or guessing which state an older save registered. The existing owner and claim checks still gate opening. Reuse the same live ownership and occupation checks for the [reunification milestones](07-reunification-of-china.md#opening-and-progress).
3. Verify the rate and staffing cap with zero, fractional, and inherited offices, at each turmoil boundary, and with each decree. Trace full and partial holdings, actual treaty ports (including Macao), occupation, recapture, a split or merge, incorporation completion, the Taiping fork, tag changes, and a victorious revolution. Check that switching decrees cannot stack effects. On save reload, confirm the old completion flag still prevents duplicate registration and the conscription bonus stays off.
4. Run standalone Tiger and `git diff --check` after scripting. Vanilla’s Algerian Departments journal uses native incorporation for overseas states. The first user playcheck should confirm that Tungning can likewise start with a single coastal foothold across the strait and that the AI starts ordinary homeland projects. If native eligibility blocks those projects, revisit the clock before adding a bypass. Keep global incorporation, AI, and migration rules outside this change.

Also trace the rules that surround integration:

- A full region and a region with only a foreign treaty-port enclave outstanding each qualify.
- Guangdong qualifies without Macao while Macao remains a treaty port. If Macao becomes an ordinary foreign holding, mark Guangdong incomplete.
- An ordinary province outstanding, ownership of only a treaty port, occupation, and ownership by a subject each fail the journal milestone. Directly held ordinary parts of a region still use the integration rate and policies.
- Check the same opening after reassertion, after final renunciation, and while Qing’s offer is pending.
- Check mobilization when a Qing war ends early, when war continues past expiry, when Qing backs down before war, and when a peace transfer forces reassertion. Verify that only the no-war case triggers the penalty and that each case unlocks the constitutional debate once.
- Check the decision with no eligible targets, split ownership, and a truce. Verify that only the preset demands avoid infamy. Vanilla reference: the Balkan War button and play in `common/scripted_buttons/00_balkan_wars_buttons.txt` and `common/diplomatic_plays/00_diplomatic_plays.txt`.
- Check simultaneous acquisition, automatic registration with just one region, and loss and recovery after registration. Verify that the outcome does not repeat on reload.
- Vanilla references: `map_data/state_regions/11_east_asia.txt` (regions) and `common/treaty_articles/14_treaty_port.txt` (treaty-port status).
