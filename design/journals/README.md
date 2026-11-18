# Tungning journal entries

Design drafts for Tungning’s campaigns, set in the world described in [storyline.md](../../storyline.md). Numbers are starting balance targets.

| Entry | Opens | Resolves into |
| --- | --- | --- |
| [The Claim Across the Strait](01-mainland-claim.md) | 1836 | Reassert, renounce, or face a final choice when Taiping rises |
| [The Faith of the Court](02-court-faith.md) | 1836 | Catholicism, Protestantism, Confucianism, or Mahayana Buddhism |
| [The Southern Passage](03-dutch-east-indies.md) | After the opening diplomacy retry, with a southern holding and a Dutch rival | Secure the remaining holdings or concede them |
| [The Manila Question](04-philippines.md) | Spain leaves the overlord chain; the opportunity starts once Manila is independent | Establish Tungning rule over the Philippines or let the opportunity pass |
| [Who Shall Rule the Eastern Sea?](05-constitutional-settlement.md) | After final renunciation or the end of reassertion mobilization | A republic, a restored Ming court, or a Zheng monarchy |
| [The Return to the Mainland](06-mainland-reconquest.md) | Reassertion or recovery of a coastal foothold | Establish an administration in any one of Fujian, Guangdong, or Zhejiang |
| [The Reunification of China](07-reunification-of-china.md) | Tungning establishes its first mainland administration | Reunite China by direct rule or provincial charters; settle the capital, Taiwan, and the southern holdings |
| [The Enemy of Our Enemy](08-taiping-rebellion.md) | The actual Taiping Rebellion begins | Commit or abandon an unsettled claim; negotiate aid and postwar terms if Tungning reasserts |

## How the journals fit together

- Faith and the southern dispute run alongside the mainland debate. Manila’s opening depends on its own overlord and ownership checks.
- Reassertion settles the claim immediately and starts mobilization. It makes a Qing play available and delays the constitutional debate until mobilization ends.
- The claim has no calendar deadline. If a foothold is already owned when Taiping rises, it resolves the claim first. Otherwise a claim still unresolved, including a pending Qing offer, reaches a mandatory fork. An earlier reassertion makes the wartime pact optional.
- One administered coastal region opens reunification. That entry carries over the three coastal objectives and checks mainland owners and charters even if the Qing government splits or changes tags.
- Becoming a Qing tributary does not by itself remove Tungning’s southern subjects or pause the other journals. Native subject restrictions still apply.
- Any final renunciation permanently closes the Ming track. Only the explicit abandonment at the Taiping fork also closes the scripted mainland campaign.

## Shared implementation

- **Files:** Add entries in `common/journal_entries/`, bars in `common/scripted_progress_bars/`, and actions in `common/scripted_buttons/`. Add namespaced localization, events, effects, triggers, and modifiers alongside them.
- **Scope:** Run the chain for the living country created as `TWG` by this mod. Use the founding marker through any vanilla tag change. Start the court debates after setup and record the actual southern holdings after the existing day-eight diplomacy retry.
- **Opening effects:** Apply the mainland, faith, southern, and constitutional modifiers when their relevant phase opens. Show them in the journal and remove them when that phase ends or a state no longer qualifies. Keep the starting forces in the 1836 setup so reopening a journal cannot grant them again.
- **Ownership:** Check the mainland foothold after relevant changes (`on_state_owner_change`, `on_state_created`) and on a country pulse. Recheck on load or when a scheduled event arrives. Use current treaty-port state status; check the foothold before resolving an unsettled claim.
- **Bars and events:** Apply action and event changes immediately and sum routine drift monthly. Mainland and faith resolve at their endpoints; the Taiping fork freezes the mainland bar and constitutional mandates unlock ratification actions. A pending Qing offer, a pending fork, or a resolved journal cannot receive old court events.
- **Display:** Show what moves each bar, what each choice costs, when temporary effects end, and why an action is blocked.
- **Persistence:** Track mainland stance, Qing offer, Taiping conflict and terms, mobilization, foothold registration, and proclamation separately. Track seat preparations and ratified charters against their actual holder. Record each outcome before granting rewards and clear temporary effects when their conditions end.
- **Compatibility:** Use vanilla interest groups, ideologies, laws, religions, country tags, and subjects. Add the coastal claim play and listen for Taiping from appended on-actions without replacing vanilla files or UI. A player or AI decision starts or joins a play; journals alone do not start wars.

Build the claim and faith entries first, including the Taiping launch check and the shared ownership test. Add the foothold and mobilization cleanup, then build Taiping’s negotiated aid and settlement and the constitutional opening. Add the reunification map and charters before the seat and autonomy events. The southern and Manila journals can be built separately; their settlement hooks make any remaining holdings eligible for the southern compact.

## Static verification

- Check keys, scopes, and hooks against installed vanilla scripts. Examples: state hooks in `common/on_actions/00_code_on_actions.txt`, two-ended bars in `common/journal_entries/01_paris_commune.txt`, parallel bars in `common/journal_entries/01_french_monarchism.txt`, and cooldowns and AI choices in `common/scripted_buttons/00_scripted_buttons.txt`.
- Run standalone Tiger and `git diff --check` after implementation. Trace deadlines, tie breaks, pending events, target changes, and reward cleanup.
- Leave runtime balance and UI checks to the user, per [AGENTS.md](../../AGENTS.md). The draft does not retrofit campaigns that passed the mod’s opening setup before the journals were installed.
