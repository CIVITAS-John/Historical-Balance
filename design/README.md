# Tungning journal entries

Design drafts for approval. The journals start from the world described in [storyline.md](../storyline.md). All numbers are starting balance targets.

| Entry | Opens | Resolves into |
| --- | --- | --- |
| [The Claim Across the Strait](01-mainland-claim.md) | 1836 | Reassert the claim or renounce it and seek Qing’s terms; a mainland foothold forces reassertion while the claim is unresolved |
| [The Faith of the Court](02-court-faith.md) | 1836 | Catholicism, Protestantism, Confucianism, or Mahayana Buddhism |
| [The Southern Passage](03-dutch-east-indies.md) | After the opening diplomacy retry, with a southern holding and a Dutch rival | Secure the remaining holdings or concede them |
| [The Manila Question](04-philippines.md) | Spain leaves the overlord chain; the opportunity starts once Manila is independent | Establish Tungning rule over the Philippines or let the opportunity pass |
| [Who Shall Rule the Eastern Sea?](05-constitutional-settlement.md) | After the mainland claim is settled | A republic, a restored Ming court, or a Zheng monarchy, each with its own follow-up |
| [The Return to the Mainland](06-mainland-reconquest.md) | Tungning regains Fujian, Guangdong, or Zhejiang apart from treaty-port enclaves | Secure all three state regions |

## How the journals fit together

- Faith and the southern dispute run alongside the mainland debate.
- Becoming a Qing tributary does not by itself remove Tungning’s southern subjects or pause the other journals. Native subject restrictions still apply.
- Final renunciation permanently closes the Ming track. Later independence or mainland reconquest does not reopen it.
- The Philippine opening depends on Manila’s situation. It does not require a mainland or constitutional outcome.

## Shared implementation

- **Files:** Add entries in `common/journal_entries/`, bars in `common/scripted_progress_bars/`, and actions in `common/scripted_buttons/`. Add namespaced localization, events, effects, triggers, and modifiers alongside them.
- **Scope:** Run the chain for the living `TWG` created by this mod. Start the court debates after setup and record the actual southern holdings after the existing day-eight diplomacy retry.
- **Ownership:** Check the mainland foothold after relevant changes (`on_state_owner_change`, `on_state_created`) and on a country pulse. Recheck on load or when a scheduled event arrives. Use current treaty-port state status; check the foothold before resolving an unsettled claim.
- **Bars:** Apply action and event changes immediately and routine drift monthly. Resolve the mainland and faith endpoints in the effect that reaches them. The constitutional bars unlock ratification actions.
- **Display:** Show drift, deadlines, disabled action reasons, and outcome recaps.
- **Persistence:** Record the mainland stance and diplomatic result, the reconquest journal’s opening and completion, the faith settlement, and the constitutional route separately. Keep phase, cooldown, and deadline state separate from results. Record outcomes before applying rewards.
- **Guards:** Recheck relevant ownership, rank, laws, rivals, and eligibility. Apply each outcome once and remove modifiers when their conditions end. Keep checking for the first mainland foothold even after the claim debate is settled.
- **Compatibility:** Use vanilla interest groups, ideologies, laws, religions, country tags, subjects, and plays. Add effects locally or nationally as specified. Do not replace vanilla files or UI, add map claims beyond the named objectives, or start wars by script.

Build mainland and faith first. Add the mainland follow-up against the shared ownership check, and the southern and Manila journals against verified ownership and diplomacy hooks. Build the constitutional panel and its follow-ups once the mainland settlement flag is reliable.

## Static verification

- Check keys, scopes, and hooks against installed vanilla scripts. Examples: state hooks in `common/on_actions/00_code_on_actions.txt`, two-ended bars in `common/journal_entries/01_paris_commune.txt`, parallel bars in `common/journal_entries/01_french_monarchism.txt`, and cooldowns and AI choices in `common/scripted_buttons/00_scripted_buttons.txt`.
- Run standalone Tiger and `git diff --check` after implementation. Trace deadlines, tie breaks, pending events, target changes, and reward cleanup.
- Leave runtime balance and UI checks to the user, per [AGENTS.md](../AGENTS.md). The draft does not retrofit campaigns that passed the mod’s opening setup before the journals were installed.
