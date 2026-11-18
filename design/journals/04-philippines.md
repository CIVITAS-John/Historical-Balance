# The Manila Question

The Manila Compact was a bargain with Spain. If Manila breaks away, Tungning can build a relationship with the new government, seek its submission, or demand territory through a normal diplomatic play.

## Opening

- **Entry:** `fh_je_manila_question`. Show it while the Philippines (`PHI`) owns Manila city (`p:x0D8236`) and Spain is absent from its entire overlord chain.
- **Window:** Start the eight-year clock the first time an independent Philippines meets those conditions. If it serves another power, show why the opportunity is blocked. An annexed Philippines cannot open it.
- **Suspension:** If Manila changes hands or the Philippines loses independence, check first for qualifying Tungning submission or conquest. Otherwise suspend new actions and cancel pending events until independent `PHI` again owns Manila. The clock keeps running and cannot restart.

## Prepare the approach

- **Send Envoys to Manila:** Once per journal, open an audience if Tungning is at peace with the Philippines, has an active interest in Indonesia, has at least +20 relations, and shares no active trade or investment accord with Manila. Gain +5 relations, or +10 if Tungning is Catholic. Give the Industrialists +2 approval and reduce available bureaucracy by 5% for six months.
- **Prepare a Crossing:** Requires peace, an active interest in Indonesia, no default, at least five regular battalions, naval projection at least equal to the Philippines’, and a legal subjugation or territorial goal. Once per journal, lose 10 relations and give the Armed Forces +2 approval and Industrialists −2 for a year. For that year, Tungning gains +10% naval invasion efficiency and pays +5% military goods costs.
- **Trade ties:** Seek trade privileges or investment rights through normal diplomacy when legal. Each side can refuse. An agreement supports the diplomatic approach but does not complete the journal.
- **Choice:** The two journal actions share a six-month cooldown. Neither is required for either route. The window does not extend when an action or event fires.

## Events

Each quarter during the open window, roll a 10% chance to draw one eligible event. Start a shared 12-month event cooldown on draw. Recheck eligibility when answered; unanswered events or responses during suspension, a deadline hold, or after closure have no effect.

| Event | Eligible while Tungning is at peace with Manila and… | Choices |
| --- | --- | --- |
| Manila merchants seek a new partner | Relations are at least +20 | Welcome the delegation (+5 relations, −5% bureaucracy) or leave trade to private brokers (+2 Industrialist approval). |
| Officers report an opening | Manila is fighting another war or turmoil in its Manila state is at least 15% | Send observers (−5 relations, +5% naval invasion efficiency, +5% military goods costs) or reassure Manila (+5 relations). |
| Missionaries cross the strait | Tungning is Catholic | Receive them (+5 relations, +2 Devout approval, −2 Intelligentsia approval) or keep the audience private (+2 Intelligentsia approval). |

Event modifiers last six months. An event cannot sign an agreement, grant territory, or start a play.

## Establish Tungning rule

- **Submission:** Become the direct overlord of the Philippines while it still owns Manila. Use a legal native agreement where available, or enforce a native subjugation demand. Make Tributary and Make Protectorate depend on vanilla rank and recognition rules. Keep the Philippine tag and its vanilla content.
- **Conquest:** When the window starts, record provinces `PHI` owns in Luzon and the Visayas. Tungning must directly own Manila, more than half of the recorded set, and Cebu (`p:xD2CA4A`) if that city was in the set. Require a territorial goal enforced in a qualifying play against the Philippines. Occupation and land taken from an unrelated country cannot satisfy the route by themselves.
- **Qualifying play:** Tungning must initiate it against independent `PHI` during the window and demand Philippine submission or territory. Record enforcement before checking ownership, so a goal that extinguishes `PHI` can still count for conquest.
- **Deadline:** Wait for a qualifying play that is already underway at expiry, and record its identity. No new play extends the window.

## Outcomes, AI, and static checks

- **Success:** Grant +10 prestige for five years and recap direct rule or rule through Manila. On expiry, close without a territorial penalty. End any journal preparations when the entry closes.
- **AI:** Start with envoys or legal agreements when relations make cooperation plausible. Consider a play when Manila is distracted by war or turmoil, Tungning can field land and naval forces, and likely third-party intervention is manageable. Recheck interests, eligibility, finances, and existing diplomacy before committing. Other journals do not gate Manila.
- **Display:** Show deadline, progress toward each route, and concrete blockers such as rank, missing interests, subject restrictions, or a third-party overlord.
- **Verify:** Spanish rule, independent Manila, a third-party handover, renewed Spanish authority, expired preparations, successful submission, and conquest that extinguishes `PHI`.
- Vanilla: `common/history/diplomacy/00_subject_relationships.txt` (Spanish colony), `common/journal_entries/06_philippines_je.txt` (Philippine independence), `map_data/state_regions/12_indonesia.txt` (Luzon and the Visayas), and `common/diplomatic_plays/00_diplomatic_plays.txt` (native plays).
