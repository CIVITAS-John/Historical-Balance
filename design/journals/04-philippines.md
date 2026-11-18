# The Manila Question

When Spain can no longer speak for Manila, Tungning can seek control through diplomacy or war. The journal itself transfers no land and does not make the Philippines surrender.

## Visibility and deadline

- **Entry:** `fh_je_manila_question`.
- **Visible when:** The Philippines (`PHI`) is alive, owns Manila city (`p:x0D8236`), and Spain is absent from its entire overlord chain.
- **Blocked by another overlord:** If Spain transfers its colony to another power, show the journal as blocked until the Philippines gains independence.
- **Does not open:** Spain annexes the Philippines outright, or a surviving Philippine government no longer owns Manila. In the latter case, Manila must be regained first.
- **Opportunity:** Start the eight-year window the first time the independent Philippines meets the visibility conditions. The other journals do not gate it.
- **Suspension:** Suspend new actions if Spain reasserts authority or another power takes over Manila or the Philippine government. Check for qualifying Tungning submission or conquest before applying suspension.
- **Expiry:** The deadline keeps running during suspension and cannot restart. Ordinary diplomacy remains available after the journal expires.

## Courses of action

### Send envoys to Manila

- **Requires:** An active interest in Indonesia, peace with the Philippines, and at least +20 relations.
- **Optional:** A five-year trade or investment agreement through normal diplomacy supports the approach but does not complete the journal.
- **Audience:** A Catholic Tungning without an existing Philippine accord can gain +10 relations once. The journal itself has no religious requirement.

### Seek submission

- **Route:** Use a legal native play or a native peaceful subject agreement where available.
- **Rank and recognition:** Unrecognized Tungning can press Make Tributary when rank permits. Recognized Tungning can pursue a protectorate when eligible.
- **Completion:** Tungning becomes the direct overlord of `PHI`, which still owns Manila. Keep the Philippine tag and its vanilla content.

### Take the islands

- **Baseline:** At the start of the window, record the provinces owned by `PHI` in Luzon and the Visayas.
- **Required ownership:** Tungning must directly own Manila and more than half of that recorded set. Require Cebu (`p:xD2CA4A`) too if the Philippines owned it at opening.
- **Exclusions:** Occupation alone does not qualify. Local rulers’ parcels outside the recorded set and Mindanao are not required.
- **Completion:** Require the ownership above and a corresponding enforced goal in a qualifying play. Land gained from an unrelated country without that goal does not count.

## Qualifying plays

- **Start:** Tungning must initiate the play against independent `PHI` during the open window, targeting Philippine subjugation or territory.
- **At the deadline:** Let a qualifying ongoing play finish. Store its identity and do not extend the window for another.
- **At enforcement:** Record the goal before checking the tag and ownership. Taking Manila in a settlement that extinguishes `PHI` can still complete the conquest route.
- **Display:** Show both completion routes and explain when rank, lack of an interest, Tungning’s subject status, or a third-party overlord blocks a play.

## Outcomes and static checks

- **Success:** +10 prestige for five years and a recap describing direct rule or rule through Manila.
- **Expiry:** No territorial penalty.
- **Limits:** Normal AI diplomacy can qualify. No special AI acquisition plan, broken truce, or rewritten treaty.
- **Verify:** Spanish subject, independent Manila, a transfer to a third party, renewed Spanish authority, a legal subject win, and a qualifying conquest that extinguishes `PHI`.
- **Vanilla references:** `common/history/diplomacy/00_subject_relationships.txt` (Spanish colony), `common/journal_entries/06_philippines_je.txt` (independence), `map_data/state_regions/12_indonesia.txt` (Luzon and the Visayas), and `common/diplomatic_plays/00_diplomatic_plays.txt` (native plays).
