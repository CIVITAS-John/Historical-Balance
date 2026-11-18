# The Return to the Mainland

Tungning has returned to the coast. To secure its position, it must hold the first foothold and reclaim the remaining regions.

## Opening

- **Entry:** `fh_je_mainland_reconquest`.
- **Requires:** The first time Tungning directly owns any one of **Fujian**, **Guangdong**, or **Zhejiang** under the [mainland foothold rule](01-mainland-claim.md#mainland-foothold).
- **Timing:** Open once, as soon as the ownership check passes. If the opening claim is still unresolved, settle it as **Reassert** in the same check, before opening this entry.
- **Existing settlement:** If the opening claim already ended, keep its stance and diplomatic result. Prior renunciation still bars Ming restoration.

## Objectives and completion

- Show a separate objective for each region. Use the same ownership rule for all three:
  - Fujian (`STATE_FUJIAN`).
  - Guangdong (`STATE_GUANGDONG`).
  - Zhejiang (`STATE_ZHEJIANG`).
- Update the checklist if Tungning loses or regains a region. Losing the first foothold does not reset or close the journal.
- Complete when Tungning meets the ownership rule in all three regions at once. If all three qualify at opening, complete on that check.
- Record completion once and show a recap. The journal itself grants no territory or claims and changes no treaties or constitutional route.

## Static checks

- A full region and a region with only a foreign treaty-port enclave outstanding each qualify.
- Guangdong qualifies without Macao while Macao remains a treaty port. If Macao becomes an ordinary foreign holding, mark Guangdong incomplete.
- An ordinary province outstanding, ownership of only a treaty port, occupation, and ownership by a subject each fail.
- Check the same opening after reassertion, after final renunciation, and while Qing’s offer is pending.
- Check loss and regain of the first foothold, simultaneous acquisition of all three regions, and a save loaded after completion.
- Vanilla references: `map_data/state_regions/11_east_asia.txt` (regions) and `common/treaty_articles/14_treaty_port.txt` (treaty-port status).
