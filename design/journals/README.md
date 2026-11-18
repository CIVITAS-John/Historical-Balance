# Tungning journal entries

Design drafts for Tungning’s campaigns, set in the world described in [storyline.md](../../storyline.md). Numbers are starting balance targets.

| Entry | Opens | Resolves into |
| --- | --- | --- |
| [The Claim Across the Strait](01-mainland-claim.md) | 1836 | Reassert and mobilize against Qing, or renounce and seek Qing’s terms |
| [The Faith of the Court](02-court-faith.md) | 1836 | Catholicism, Protestantism, Confucianism, or Mahayana Buddhism |
| [The Southern Passage](03-dutch-east-indies.md) | After the opening diplomacy retry, with a southern holding and a Dutch rival | Secure the remaining holdings or concede them |
| [The Manila Question](04-philippines.md) | Spain leaves the overlord chain; the opportunity starts once Manila is independent | Establish Tungning rule over the Philippines or let the opportunity pass |
| [Who Shall Rule the Eastern Sea?](05-constitutional-settlement.md) | After final renunciation or the end of reassertion mobilization | A republic, a restored Ming court, or a Zheng monarchy |
| [The Return to the Mainland](06-mainland-reconquest.md) | Tungning regains Fujian, Guangdong, or Zhejiang apart from treaty-port enclaves | Secure all three state regions |

## How the journals fit together

- Faith and the southern dispute run alongside the mainland debate. Manila’s opening depends on its own overlord and ownership checks.
- Reassertion settles the claim immediately and starts mobilization. It makes a Qing play available and delays the constitutional debate until mobilization ends.
- The first mainland foothold opens reconquest immediately. If the claim is unresolved, the foothold forces reassertion first; after settlement, it leaves the recorded stance and treaty intact.
- Becoming a Qing tributary does not by itself remove Tungning’s southern subjects or pause the other journals. Native subject restrictions still apply.
- Final renunciation permanently closes the Ming track. Later independence or mainland reconquest does not reopen it.

## Shared implementation

- **Files:** Add entries in `common/journal_entries/`, bars in `common/scripted_progress_bars/`, and actions in `common/scripted_buttons/`. Add namespaced localization, events, effects, triggers, and modifiers alongside them.
- **Scope:** Run the chain for the living `TWG` created by this mod. Start the court debates after setup and record the actual southern holdings after the existing day-eight diplomacy retry.
- **Ownership:** Check the mainland foothold after relevant changes (`on_state_owner_change`, `on_state_created`) and on a country pulse. Recheck on load or when a scheduled event arrives. Use current treaty-port state status; check the foothold before resolving an unsettled claim.
- **Bars and events:** Apply action and event changes immediately and sum routine drift monthly. Mainland and faith resolve at their endpoints; constitutional mandates unlock ratification actions. Expired choices have no effect. A pending Qing offer or a resolved journal cannot receive old court events.
- **Display:** Show what moves each bar, what each choice costs, when temporary effects end, and why an action is blocked.
- **Persistence:** Track the mainland stance, Qing offer result, mobilization, and reconquest separately. Keep cooldowns and deadlines separate from recorded outcomes. Record each outcome before granting any reward, and clear temporary effects when their conditions end.
- **Compatibility:** Use vanilla interest groups, ideologies, laws, religions, country tags, and subjects. Add the Qing claim play without replacing vanilla files or UI. A player or AI decision starts the play; journals alone do not start wars.

Build mainland and faith first. Add reconquest against the shared ownership check and pair the constitutional opening with mobilization cleanup. The southern and Manila journals can be built separately against the relevant ownership and diplomacy hooks.

## Static verification

- Check keys, scopes, and hooks against installed vanilla scripts. Examples: state hooks in `common/on_actions/00_code_on_actions.txt`, two-ended bars in `common/journal_entries/01_paris_commune.txt`, parallel bars in `common/journal_entries/01_french_monarchism.txt`, and cooldowns and AI choices in `common/scripted_buttons/00_scripted_buttons.txt`.
- Run standalone Tiger and `git diff --check` after implementation. Trace deadlines, tie breaks, pending events, target changes, and reward cleanup.
- Leave runtime balance and UI checks to the user, per [AGENTS.md](../../AGENTS.md). The draft does not retrofit campaigns that passed the mod’s opening setup before the journals were installed.
