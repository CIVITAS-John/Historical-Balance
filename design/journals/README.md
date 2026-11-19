# Tungning journal entries

Design drafts for Tungning’s campaigns, set in the world described in [storyline.md](../../storyline.md). Numbers are starting balance targets.

The [aftermath tables](outcome-modifiers.md) hold the immediate effects and timed modifiers for every final outcome, including early closures and the three constitutional follow-ups.

| Entry | Opens | Resolves into |
| --- | --- | --- |
| [The Claim Across the Strait](01-mainland-claim.md) | 1836 | Reassert, renounce, or face a final choice when Taiping rises |
| [The Faith of the Court](02-court-faith.md) | 1836 | One of four official faiths and a choice to keep, repeal, or replace the Yongli Articles |
| [The Southern Passage](03-dutch-east-indies.md) | After the opening diplomacy retry, with a southern holding and a Dutch rival | Secure the remaining holdings or concede them |
| [The Manila Question](04-philippines.md) | Spain leaves the overlord chain; the opportunity starts once Manila is independent | Establish Tungning rule over the Philippines or let the opportunity pass |
| [Who Shall Rule the Eastern Sea?](05-constitutional-settlement.md) | After final renunciation or the end of reassertion mobilization | A republic, a constitutional Ming court with a Zheng cabinet, or a Zheng monarchy |
| [The Return to the Mainland](06-mainland-reconquest.md) | Reassertion or recovery of a coastal foothold | Establish an administration in any one of Fujian, Guangdong, or Zhejiang |
| [The Reunification of China](07-reunification-of-china.md) | Tungning establishes its first mainland administration | Reunite China by direct rule or provincial charters; settle the capital, Taiwan, and the southern holdings |
| [The Enemy of Our Enemy](08-taiping-rebellion.md) | The actual Taiping Rebellion begins | Commit or abandon an unsettled claim; negotiate a coastal pact or a larger southern bargain |

## How the journals fit together

- Faith and the southern dispute run alongside the mainland debate. Manila’s opening depends on its own overlord and ownership checks.
- Reassertion settles the claim immediately and starts mobilization. It makes a Qing play available and delays the constitutional debate until mobilization ends.
- The claim has no calendar deadline. If a foothold is already owned when Taiping rises, it resolves the claim first. Otherwise a claim still unresolved, including a pending Qing offer, reaches a mandatory fork. An earlier reassertion makes the wartime pact optional.
- Halfway through incorporating one secure coastal region, Tungning can begin reunification. Both entries read the same native incorporation progress. Staffed government offices speed it up, turmoil slows it, and state decrees let the court keep local magistrates, send commissioners, or fund relief. Reunification still checks mainland owners and charters when Qing splits or changes tags.
- All three coastal regions give Tungning a choice of Taiping deals: ordinary recognition with trade, or a heavier wartime commitment for the southern interior outside Taiping’s launch territory.
- Inland gains and religious support can build a Ming mandate, but losing Taiwan makes it decline. Holding the southern passage or the Philippines builds the Zheng mandate. Under a Ming restoration the Zhu wear the crown and a Zheng heads the cabinet through the stronger of the landed and maritime blocs.
- Becoming a Qing tributary does not by itself remove Tungning’s southern subjects or pause the other journals. Native subject restrictions still apply.
- Any final renunciation permanently closes the Ming track. Only the explicit abandonment at the Taiping fork also closes the scripted mainland campaign.

## Interest groups

These are the five existing Victoria 3 interest groups with Tungning-specific names and three approval traits each. Their constituencies and opening figures are described in [the storyline](../../storyline.md#the-factions-at-wenhais-court). Leave the other three groups unchanged. Numbers below are starting values at normal strength; use vanilla approval thresholds and clout scaling.

| Vanilla group | Tungning name | Unhappy | Happy | Loyal |
| --- | --- | --- | --- | --- |
| `ig_landowners` | Ming Estates | **Estate Exemptions:** −10% plantation tax income | **The Exiles’ Correspondence:** +5% influence | **Plantation Patrons:** +10% aristocrat investment pool efficiency |
| `ig_industrialists` | Maritime Houses | **Withdrawn Shipping Credit:** −5% trade advantage | **The Strait Network:** +8% trade advantage | **Profits Back into Port:** +10% capitalist investment pool efficiency |
| `ig_devout` (Catholic or Protestant) | Catholic Missions / Reformed Congregations | **Closed Classrooms:** −3 percentage points of education access | **Church Schools:** +3 percentage points of education access | **Books from Overseas:** +8% technology spread |
| `ig_devout` (Confucian) | Ritual Academies | **Religious Petitions:** +10% radicals from political movements | **The County Schools:** +5% bureaucracy | **Keepers of the Rites:** +5% authority |
| `ig_devout` (Mahayana Buddhist) | Buddhist Temples | **Religious Petitions:** +10% radicals from political movements | **Temple Relief:** −2% mortality | **Mediators of the Villages:** −10% radicals from political movements |
| `ig_intelligentsia` | School of Practical Learning | **Public Criticism:** −5% prestige | **Surveyors and Translators:** +8% technology spread | **Open Examinations:** +8% qualifications |
| `ig_armed_forces` | Army and Fleet | **Waste in the Arsenals:** +10% military goods cost | **Joint Staff College:** +8% military technology research | **Overseas Service:** +8% naval power projection and +5% army offense |

- **Apply only to Tungning:** After its primary cultures and characters are set, use a namespaced country effect on the existing IGs. Define the names and descriptions in localization and the traits in `common/interest_group_traits/`. Use `set_interest_group_name` and `set_ig_trait` for each slot; leave vanilla group files untouched. Preserve the School’s non-anticlerical Han baseline. Verify the mod’s presentation survives a tag change without reappointing leaders at each pulse.
- **Colonial policy:** Give the Maritime Houses a scoped group ideology for overseas trade that approves Colonial Resettlement and Colonial Exploitation and disapproves No Colonial Affairs. Leave their other law preferences and Yang’s independent Market Liberal ideology in place. In the journals they favor new markets, colonies, protected trade, and migration, while opposing costly wars that could cut those routes.
- **The officers:** Add Army and Fleet leadership to the opening admiral Shi Jichang and mark him mainland-first. Future officers keep their native character ideologies. Append a Tungning-only handler to `on_new_interest_group_leader`; give an unassigned Army and Fleet leader a persistent mainland-first, southern-expedition, or neutral stance (40/40/20 as a starting split). A Pacifist is neutral regardless of the stored stance. Read the *current group's leader*, with a neutral fallback for no leader, in approval, drift, and AI choices. Do not block lawful actions or start plays based on the leader alone.
- **The Devout:** Setup installs the Catholic Missions. Only [settlement of the faith journal](02-court-faith.md#settlement) changes the scripted identity and religious leadership; a nomination can influence constitutional arguments without changing the official religion, support, or Taiping willingness. Let native faith laws operate in their own right. The Christian traits and the existing mission-school and Manila choices represent Western learning without borrowing a vanilla Westernization journal.

## Shared implementation

- **Files:** Add entries in `common/journal_entries/`, bars in `common/scripted_progress_bars/`, and actions in `common/scripted_buttons/`. Add namespaced localization, events, effects, triggers, and modifiers alongside them.
- **Scope:** Run the chain for the living country created as `TWG` by this mod. Use the founding marker through any vanilla tag change. Start the court debates after setup and record the actual southern holdings after the existing day-eight diplomacy retry.
- **Opening effects:** Apply the mainland, faith, southern, and constitutional modifiers when their relevant phase opens. Show them in the journal and remove them when that phase ends or a state no longer qualifies. Keep the starting forces in the 1836 setup so reopening a journal cannot grant them again.
- **Ownership:** Check the mainland foothold after relevant changes (`on_state_owner_change`, `on_state_created`) and on a country pulse. Recheck on load or when a scheduled event arrives. Use current treaty-port state status; check the foothold before resolving an unsettled claim.
- **Bars and events:** Apply action and event changes immediately and sum routine drift monthly. Mainland resolves at its endpoints; a faith endpoint opens the final church law audience and freezes the faith bar. The Taiping fork freezes the mainland bar and constitutional mandates unlock ratification actions. Court events cannot resolve during a pending offer, fork, or audience, or after their journal closes.
- **Display:** Show what moves each bar, what each choice costs, when temporary effects end, and why an action is blocked.
- **Persistence:** Track mainland stance, Qing offer, Taiping conflict and terms, mobilization, foothold registration, and proclamation separately. Track seat preparations and ratified charters against their actual holder. Use the shared [settlement and aftermath rules](outcome-modifiers.md#implementation-order) for closing effects.
- **Compatibility:** Keep vanilla interest group IDs, laws, religions, country tags, and subjects. The faith journal uses a Tungning-only change restriction in the vanilla Church and State law group; see the [law plan](../law-plan.md#implementation-and-checks). Customize Tungning’s presentation and assign only scoped traits or ideology additions. Add the coastal claim play and listen for Taiping from appended on-actions. A player or AI decision starts or joins a play; journals alone do not start wars.

1. Add the names, traits, colonial ideology, and officer stance helpers to Tungning’s [setup](../../common/scripted_effects/fh_tungning_setup.txt), with the Catholic profile refreshed only by faith settlement. Vanilla references: `common/interest_group_traits/`, `events/india_events/princely_state_creation.txt`, and `common/on_actions/00_code_on_actions.txt` (new group leader).
2. Build the opening claim and faith entries with that faction state, the shared direct ownership test, and the Taiping launch snapshot. Record the snapshot after vanilla assigns Taiping’s starting states. Keep delayed offers and journal outcomes separate.
3. Add foothold mobilization and replace the existing registration streak with the [shared mainland integration rules](06-mainland-reconquest.md#mainland-integration). Keep incorporation and decree enforcement in state scope and outside the journals’ lifetimes so the same rules apply through reunification. Spontaneous coastal migration remains separate.
4. Add Taiping’s two offers, contribution accounting, and settlement through the same transfer checks. Ordinary and expanded terms have mutually exclusive state and aid schedules. Use the native goods, ship, trade, and state treaty articles where legal.
5. Add the southern and Manila journals, recording completed outcomes and current retained holdings separately. Build the reunification map and charters before the seat and autonomy events. Have the integration bar and proclamation use the same live state checks.
6. Build the constitutional follow-ups against those territorial and faith outcomes. Mark the founding Zheng and Zhu characters with distinct `dynasty_var` values; vanilla passes that variable to new heirs. For a Ming charter store a Zhu ruler and a distinct Zheng First Minister, relying on `set_character_as_ruler`, `set_heir`, `set_interest_group`, and `set_as_interest_group_leader` for the native roles. Represent the executive title with the charter status and appointment decision, as there is no separate permanent minister slot exposed in the vanilla scripts. See `events/resignation.txt` (ruler appointment), `events/iberia_events/regency_events.txt` (heir), `common/scripted_effects/00_victoria_on_actions_effects.txt` (inherit the royal house), and `events/iberia_events/ip4_portuguese_political_events.txt` (sitting group leader used as prime minister).

## Static verification

- Check keys, scopes, and hooks against installed vanilla scripts. Examples: state hooks in `common/on_actions/00_code_on_actions.txt`, two-ended bars in `common/journal_entries/01_paris_commune.txt`, parallel bars in `common/journal_entries/01_french_monarchism.txt`, and cooldowns and AI choices in `common/scripted_buttons/00_scripted_buttons.txt`.
- Trace character succession, interest group approval thresholds, the four faith outcomes, and territorial changes across each journal that uses them. Check occupation, ownership loss, reloads, and changes of law or government before finalizing delayed events. Keep the regime and religion checks Tungning-only.
- Run standalone Tiger and `git diff --check` after implementation. Trace deadlines, tie breaks, pending events, target changes, and reward cleanup.
- Leave runtime balance and UI checks to the user, per [AGENTS.md](../../AGENTS.md). The draft does not retrofit campaigns that passed the mod’s opening setup before the journals were installed.

The design does not add new interest groups, a separate cabinet UI, colonial law paths, or a post-Qing war between Tungning and Taiping.
