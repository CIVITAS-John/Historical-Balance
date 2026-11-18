# The Return to the Mainland

Reasserting the claim gives Tungning a short window to prepare for war with Qing. The return to the mainland is a separate milestone: it begins with the first foothold, however Tungning acquires it.

## Mobilization after reassertion

- **Starts:** Apply the three-year [reassertion package](01-mainland-claim.md#reassert-the-claim) once when the court chooses Reassert, including when a foothold forces that choice. During mobilization, give AI Tungning more weight for barracks and their military supplies.
- **Ends:** Remove the package at the end of the first war in which Tungning and Qing fight on opposite sides, or after three years, whichever comes first. Count a war already in progress at reassertion and a war whose peace settlement gives Tungning the foothold that forces reassertion. A diplomatic play that ends before war does not count.
- **No war:** If the package expires without Tungning ever fighting Qing during this phase, fire **A War Never Fought** once: −3 Armed Forces approval and −5 base legitimacy for one year. If the war is still active at expiry, remove the package without the penalty.
- **Next journal:** Open the [constitutional debate](05-constitutional-settlement.md#opening) when mobilization ends. The no-war event does not extend the wait.

## Decision: Press the Mainland Claims

- **Available after Reassert:** Start a diplomatic play against Qing for any claimed state it still owns in Fujian, Guangdong, or Zhejiang that is eligible for a Return State demand. Show the demands before confirmation. Skip territory already recovered, treaty ports, and other countries’ land.
- **Diplomacy:** The preset demands carry no infamy. Use the normal play and settlement phases; check truces, subject restrictions, interests, and any other blockers before offering the play. Additional demands receive no discount. Opening either journal starts no play or war.
- **AI:** Use the decision only with at least 10 regular battalions, no default, and either Qing already fighting another war or at least 25% turmoil in one of its eligible target states. Recheck the demands and blockers when the decision is taken.

## Opening the reconquest journal

- **Entry:** `fh_je_mainland_reconquest`.
- **Requires:** The first time Tungning directly owns any one of **Fujian**, **Guangdong**, or **Zhejiang** under the [mainland foothold rule](01-mainland-claim.md#mainland-foothold).
- **Timing:** Open once, as soon as the ownership check passes. If the opening claim is still unresolved, settle it as **Reassert** in the same check, before opening this entry.
- **Existing settlement:** Keep the recorded stance and any ratified treaty. A foothold gained after settlement neither starts nor refreshes mobilization. Prior renunciation still bars Ming restoration.

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
- Check mobilization when a Qing war ends early, when war continues past expiry, when Qing backs down before war, and when a peace transfer forces reassertion. Verify that only the no-war case triggers the penalty and that each case unlocks the constitutional debate once.
- Check the decision with no eligible targets, split ownership, and a truce. Verify that only the preset demands avoid infamy. Vanilla reference: the Balkan War button and play in `common/scripted_buttons/00_balkan_wars_buttons.txt` and `common/diplomatic_plays/00_diplomatic_plays.txt`.
- Check loss and regain of the first foothold, simultaneous acquisition of all three regions, and a save loaded after completion.
- Vanilla references: `map_data/state_regions/11_east_asia.txt` (regions) and `common/treaty_articles/14_treaty_port.txt` (treaty-port status).
