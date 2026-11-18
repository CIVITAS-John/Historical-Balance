# Tungning journal entries

Design draft for approval. The journal entries start from the world described in [storyline.md](../storyline.md). All numbers are starting balance targets.

| Entry | Appears | Resolves into |
| --- | --- | --- |
| [The Claim Across the Strait](01-mainland-claim.md) | 1836 | Reassert the mainland claim or renounce it and seek Qing’s terms |
| [The Faith of the Court](02-court-faith.md) | 1836 | Catholicism, Protestantism, Confucianism, or Mahayana Buddhism |
| [The Southern Passage](03-dutch-east-indies.md) | After the opening diplomacy retry, if Tungning has southern holdings and a Dutch competitor | Contest Dutch pressure or lose the opening tributaries and direct rule of Lanfang |
| [The Manila Question](04-philippines.md) | Spain loses its overlordship; the opportunity starts once Manila is independent | Establish Tungning rule over the Philippine government or let the opportunity pass |
| [Who Shall Rule the Eastern Sea?](05-constitutional-settlement.md) | After the mainland question is settled | A republic, a restored Ming court, or recognition of the Zheng dynasty, each with its own follow-up |

Faith and the southern dispute run alongside the mainland question. Becoming Qing’s tributary does not, by itself, remove Tungning’s southern subjects or pause those journals. Native subject restrictions still apply. Renouncing the mainland permanently locks the Ming track in this chain, even if Tungning later becomes independent. The Philippine opening depends on Manila’s situation, not the outcome of either court debate.

## Shared implementation

1. Add journals in `common/journal_entries/`, bars in `common/scripted_progress_bars/`, actions in `common/scripted_buttons/`, and namespaced localization, events, effects, triggers, and modifiers. Scope every entry to the living `TWG` created by this mod. Start the two court debates after opening setup, and record what was actually acquired after the existing eight-day diplomacy retry (`common/on_actions/fh_tungning_on_actions.txt:15–25`). Use a country pulse for later gates and checks; avoid scanning other countries unless an entry needs the result.
2. Route bar changes through an entry-specific calculation and resolver. Apply actions and events immediately; apply routine drift monthly. The mainland and faith bars force a decision in the same effect that reaches an endpoint. The three constitutional bars instead unlock ratification actions. Use popups as recaps and record outcomes before granting rewards. Show current drift, deadlines, and the reason for disabled actions. Tick effects do nothing once an outcome is recorded.
3. Persist one mainland stance, its diplomatic result, one faith settlement, and one constitutional route using namespaced country variables. Keep phase, cooldown, and deadline state separately. On load or when a scheduled event arrives, recheck ownership, rank, current laws, rival identities, and eligibility. Process one terminal outcome per entry, and remove timed or conditional modifiers when their conditions end.
4. Use vanilla interest groups and leader ideologies as the factions’ political base. Apply approval to the relevant interest groups and short, local or national modifiers to Tungning. Use existing laws, religions, country tags, native subjects and diplomatic plays. No vanilla file or UI replacement, no new map claims outside the named objectives, and no automatic war.

Build mainland and faith first, including their endpoint resolution. Add the southern and Manila journals against verified ownership and diplomatic hooks. Build the constitutional panel and its follow-ups after the mainland settlement flag is reliable.

The installed 1.15 scripts show two-ended bars in `common/journal_entries/01_paris_commune.txt:95–100,172–220`, three concurrent bars in `common/journal_entries/01_french_monarchism.txt:29–31,54–56,128–146`, and buttons with cooldowns and AI choices in `common/scripted_buttons/00_scripted_buttons.txt:107–168`. Paradox also describes the [journal interface and its progress bars](https://www.paradoxinteractive.com/games/victoria-3/news/dev-diary-78-update-1-2-changelog). Use these patterns without copying their event chains.

Static verification after approval: resolve every referenced key and scope against installed vanilla data, run standalone Tiger and `git diff --check`, then trace endpoints, rejected offers, tie breaks, target changes, saves with pending events, and reward cleanup. Leave runtime balance and UI checks to the user, per [AGENTS.md](../AGENTS.md). This draft does not include a retrofit for campaigns that already passed the mod’s opening setup before these journals were installed.
