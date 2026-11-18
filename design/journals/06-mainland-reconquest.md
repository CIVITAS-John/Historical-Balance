# The Return to the Mainland

The first task is to establish a government on the mainland that can survive the next war. Fujian, Guangdong, or Zhejiang can serve as that foothold. Holding one is enough to begin the larger campaign.

## Opening

- **Entry:** `fh_je_mainland_foothold`. Open on recorded reassertion, including through the [Taiping fork](08-taiping-rebellion.md#the-last-chance), or when Tungning first meets the [ownership rule](01-mainland-claim.md#mainland-foothold). If an unsettled claim resolves through ownership, record reassertion before opening this entry. While the Taiping fork awaits an answer, record any foothold gained but hold this entry closed until the court reasserts.
- **Existing settlement:** Ordinary renunciation does not sponsor a mainland campaign, but a later qualifying foothold can still open this entry without reviving Ming restoration, starting mobilization, or changing a Qing treaty. Permanent abandonment at the Taiping fork bars this entry entirely.
- **Display:** Show all three possible footholds with the outstanding ordinary land and its current owners. Losing land updates the display; the journal stays open.

## Mobilization after reassertion

- **Starts:** Apply the three-year [reassertion package](01-mainland-claim.md#reassert-the-claim) once when the court chooses Reassert, including when a foothold forces that choice. During mobilization, give AI Tungning more weight for barracks and their military supplies.
- **Ends:** Remove the package after three years or at the end of the first war in which Tungning fights Qing or its successor central government, whichever comes first. Count a war already in progress at reassertion and a war whose peace settlement forces reassertion. If Tungning reasserts at the Taiping fork while the rebellion is active, also end mobilization when that rebellion ends; fighting or actually delivering pact aid counts as following through. Answering the fork after the rebellion ends starts ordinary mobilization.
- **No war:** If the package ends without qualifying action, fire **A War Never Fought** once: −3 Armed Forces approval and −5 base legitimacy for one year. A backdown or a signed but unfulfilled pact does not count; a war still active at expiry does.
- **Defeat:** If the first tracked war ends in defeat for Tungning, apply −5 base legitimacy for one year. This can still happen if the three-year mobilization expired during that war.
- **Next journal:** Open the [constitutional debate](05-constitutional-settlement.md#opening) when mobilization ends. The no-war event does not extend the wait.

## Decision: Press the Mainland Claims

- **Available after Reassert:** Target one eligible owner at a time and assemble Return State demands for its claimed ordinary holdings in Fujian, Guangdong, and Zhejiang. This can target Qing or an eligible mainland successor that actually holds the land. Skip territory already recovered, treaty-port enclaves, and ordinary holdings of unrelated foreign powers. Suspend the preset play against Taiping while the wartime pact is in force; use its settlement process.
- **Diplomacy:** Only the preset coastal demands carry no infamy. Use normal play and settlement phases; check truces, existing conflicts, subject restrictions, interests, and eligibility. Show the target and demands before confirmation and recalculate them if control changes. Keep this action available in the reunification entry for unresolved coastal claims.
- **AI:** Use the decision only with at least 10 regular battalions, no default, a manageable opposing coalition, and either the target already fighting another war or at least 25% turmoil in one of its eligible target states.

## Consolidate the foothold

Choose **Register the Mainland Administration** once a qualifying state has two staffed levels of Government Administration and is free from enemy occupation. Tungning need only secure one region. The other two carry over into [The Reunification of China](07-reunification-of-china.md).

The first time any region qualifies by ownership, **The Magistrates at the Landing** offers a two-year choice for one qualifying state:

| Choice | Benefit | Cost |
| --- | --- | --- |
| Retain local magistrates | +10% tax capacity while the mainland offices take shape | −2 Armed Forces approval |
| Send Taiwan commissioners | +10% construction efficiency in the state | −5% bureaucracy countrywide while staff are seconded |

Recheck ownership before applying the choice. If no region still qualifies, defer the audience until one does. Remove the package if Tungning loses the selected state, even if it holds another. The event and the registration are independent: the player can consolidate without waiting for the audience.

Registration records completion once and opens reunification and the [capital discussions](07-reunification-of-china.md#where-the-government-sits). It does not incorporate the state, move the capital, or grant more land. If Tungning later loses every foothold, the completed entry stays closed and reunification pauses national actions until one is recovered. Legal coastal recovery plays remain available.

## Static checks

- A full region and a region with only a foreign treaty-port enclave outstanding each qualify.
- Guangdong qualifies without Macao while Macao remains a treaty port. If Macao becomes an ordinary foreign holding, mark Guangdong incomplete.
- An ordinary province outstanding, ownership of only a treaty port, occupation, and ownership by a subject each fail.
- Check the same opening after reassertion, after final renunciation, and while Qing’s offer is pending.
- Check mobilization when a Qing war ends early, when war continues past expiry, when Qing backs down before war, and when a peace transfer forces reassertion. Verify that only the no-war case triggers the penalty and that each case unlocks the constitutional debate once.
- Check the decision with no eligible targets, split ownership, and a truce. Verify that only the preset demands avoid infamy. Vanilla reference: the Balkan War button and play in `common/scripted_buttons/00_balkan_wars_buttons.txt` and `common/diplomatic_plays/00_diplomatic_plays.txt`.
- Check loss before answering the magistrates, simultaneous acquisition of all three regions, registration with only one region, and loss and recovery after registration. Verify that the recap and modifiers do not repeat on reload.
- Vanilla references: `map_data/state_regions/11_east_asia.txt` (regions) and `common/treaty_articles/14_treaty_port.txt` (treaty-port status).
