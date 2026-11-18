# Who Shall Rule the Eastern Sea?

Once the mainland claim is settled, the court can build a mandate for a republic, a constitutional Ming restoration, or continued Zheng rule. The mainland and the southern seas give the two royal houses different arguments. Crown a Zhu and the Zheng govern through the assembly; keep a Zheng on the throne and the family claims the mandate in its own right.

## Opening

- **Entry:** `fh_je_constitutional_settlement`.
- **Requires:** Final renunciation, including abandonment at the Taiping fork, or reassertion followed by the [end of mobilization](06-mainland-reconquest.md#mobilization-after-reassertion). A pending Qing offer, an unanswered Taiping fork, or an active mobilization keeps the debate closed.
- **Display:** Show all three bars. After final renunciation, show the Ming bar at zero and explain the permanent lock.
- **Subjects:** The Republic and Zheng routes are available to a Qing tributary. A constitutional change does not end the relationship or remove other subject restrictions.
- **Opening effect:** The rival mandates give Tungning **−5 base legitimacy** while the debate is open. Remove the penalty on ratification, before checking the follow-up’s legitimacy requirement.

## Mandates

Each mandate runs from **0 to 200**. Sum monthly drift before applying it. Apply the caps after every change, including when Ming eligibility changes.

### Republic

- **Starts at:** 30.
- **Monthly drift:** +1 if a Radical or Reformer leads the governing Intelligentsia or Trade Unions; +1 under Census Voting or Universal Suffrage; −1 under Autocracy.
- **Action:** **Convene a Civic Congress** with backing from the governing School of Practical Learning or Trade Unions. The scholars make a case for examinations and public schools under an elected government. The Ming Estates take the approval penalty.

### Ming restoration

- **Starts at:** 50 after reassertion; locked at zero after renunciation.
- **Monthly drift:** +1 if a Traditionalist or Royalist leads a governing group and −1 while Tungning is a subject. Add only the highest mainland tier:

| Mainland reach | Ming mandate each month |
| --- | ---: |
| One qualifying coastal region | +1 |
| A coastal region and at least one other fully held core region | +2 |
| A coastal region and either at least four other fully held core regions or directly held Nanjing or Beijing | +3 |

Count inland reach from the [reunification core](07-reunification-of-china.md#opening-and-progress), excluding Fujian, Guangdong, and Zhejiang. Use the same direct ownership and treaty-port rules. Chartered subjects and occupations do not count. The court loses **8 points each month** it does not directly hold ordinary Taiwan under the same ownership rule or Taiwan is under enemy occupation. Loss of Taiwan outweighs even the strongest mainland and faith support.

- **While the faith debate is active:** Add +1 if the ancestral side leads the bar and has nominated Confucianism; subtract 1 if the Christian side leads with a Christian nomination and the Catholic Missions are in government. During the settlement audience, use the frozen bar and nominations until the court acts. A tie, no leading nomination, or an interrupted debate gives no drift. This measures support for the rites in the proposed constitution; it changes neither official faith nor Devout identity.
- **After the faith debate:** Add +2 under a settled Confucian court or +1 under a settled Mahayana court. Under a settled Catholic or Protestant court, subtract 1 only if State Religion is in force; a church settlement under Freedom of Conscience or Total Separation has no penalty. If a later native law changes the official religion away from the settled faith, stop using that outcome’s drift. No faith can block restoration.
- **Action:** **Invite the Zhu Court** with backing from the governing Ming Estates, or the governing Devout while they are the Ritual Academies. The invitation promises to recognize the estates, titles, and public rites of the Zhu court. The Maritime Houses take the approval penalty.
- **Requires for invitation and ratification:** Independence, direct and unoccupied Taiwan, and a current [mainland foothold](01-mainland-claim.md#mainland-foothold). An open reconquest journal by itself does not qualify.
- **Cap:** While any requirement is missing, cap the mandate at 150 and explain what is missing.

### Zheng dynasty

- **Starts at:** 70.
- **Monthly drift:** +1 under Monarchy with legitimacy of at least 60; +1 while the Armed Forces are in government; −1 under a Presidential or Parliamentary Republic.
- **The southern mandate:** Add **+2 per month** after successfully securing [The Southern Passage](03-dutch-east-indies.md#outcomes), while Tungning still holds any recorded southern grant from that settlement. Add another **+2** while the Philippines is under Tungning: either Manila is held by directly subject `PHI`, or Tungning directly owns Manila and still meets the [Manila journal’s conquest ownership threshold](04-philippines.md#establish-tungning-rule). If that journal never recorded a starting set, require Manila, Cebu, and more than half of the ordinary provinces of Luzon and the Visayas. This check can credit native diplomacy or conquest after the window closes. The two bonuses stack, disappear separately on loss, and never require a faith or mainland foothold. Opening holdings alone do not count as securing the passage.
- **Action:** **Petition for a Zheng Mandate** with backing from the governing Army and Fleet or Ming Estates. Either officer wing can back the Zheng dynasty. The School of Practical Learning takes the approval penalty.

## Endorsements

All three actions share a six-month cooldown. Add 12 to the chosen mandate and subtract 5 from each rival. For six months, give the supporter +2 approval and the named opponent −2. If both possible supporters qualify, use the first listed. Record the last explicit endorsement.

## Court events

Each quarter, roll a 10% chance to draw one eligible petition. Petitions share a 12-month cooldown. Backing a petition adds 5 to its mandate and gives the petitioning group +1 approval for six months; rejecting it subtracts 5 and gives that group −1. Neither option counts as an endorsement. Recheck eligibility before applying either choice.

| Petition | Eligible while | Approval group |
| --- | --- | --- |
| Civic delegates | Census Voting or Universal Suffrage | Intelligentsia |
| Zhu envoys | Tungning reasserted, is independent, and holds both Taiwan and a foothold under the invitation rules | Ming Estates |
| Zheng officers | Army and Fleet in government | Army and Fleet |
| Petition from the southern ports | Either southern mandate condition is active | Maritime Houses |

## Ratification

- **Threshold:** A mandate at 200 unlocks its **Ratify** action while it remains eligible. There is no forced choice or deadline.
- **Recommendation:** If several mandates are ready, highlight the last explicit endorsement if it is ready. Otherwise prefer Zheng, then Republic, then Ming.
- **Selection:** Offer a negotiated compact or a decisive proclamation for the selected mandate. Recheck eligibility when confirmed, record the route and tone, apply the [ratification aftermath](outcome-modifiers.md#constitutional-debate), and open the follow-up once. The AI favors a route that fits its laws, government, and holdings; default to a compact unless the winning mandate leads each rival by at least 50 points.

## Follow-up journals

For each route, maintain the listed ongoing requirements for six consecutive months. Reset the streak when any of them fails. Recheck eligibility before recording completion. Each follow-up uses its own aftermath; the ratification tone does not change its requirements or effects.

### The Taiwan Convention — Republic

- **Requires:** Parliamentary Republic or Presidential Republic enacted through normal law play.
- **Requires:** Wealth Voting, Census Voting, or Universal Suffrage.
- **Requires:** Legitimacy of at least 60.
- **Effects:** Display **Republic of Tungning** while a valid republican law is active. Apply [The Taiwan Convention’s aftermath](outcome-modifiers.md#the-taiwan-convention) on completion.
- **Continuity:** Keep the same playable country, subjects, treaties, religion, and surviving claims.

### The Southern Court Reborn — Ming restoration

- **Requires:** Independence, Monarchy, a voting law (Landed Voting, Wealth Voting, Census Voting, or Universal Suffrage), directly held and unoccupied Taiwan, the current mainland foothold, and legitimacy of at least 60. Enact voting and Monarchy through ordinary law play. The stronger eligible group between the Ming Estates and Maritime Houses must be in government. Compare their current clout if both are non-marginalized; break a tie for the Ming Estates. If one is marginalized use the other, and if neither qualifies the cabinet cannot be formed.
- **If a requirement is lost:** Pause the follow-up and reset the streak. Show which group must enter government and update that requirement if clout changes. Recheck the coalition, laws, territory, and both officeholders before completion.
- **A Zhu crown:** Prefer the living, local Prince Zhu Yucheng (`fh_tungning_ming_claimant`); otherwise prepare a Zhu cadet once. Make Zhu the monarch. Remove any non-Zhu heir from the line of succession without exiling them, and use an eligible Zhu heir or prepare a Zhu cadet for that role. Mark the Zhu dynasty for native inheritance so future heirs belong to the same house. In the charter and court events the monarch presides at ceremonies and represents the state; he does not claim the personal authority of the old imperial throne.
- **A Zheng cabinet:** Have the Zheng incumbent step down by agreement if one reigns. Use that adult Zheng as **First Minister** if still eligible after the handover; otherwise choose a living adult Zheng in Tungning (prefer the outgoing Zheng heir if eligible) or create one cadet. Record the dynastic office separately from the native ruler. Assign the First Minister to the stronger bloc as its actual interest group leader. The other Zheng branch can still join the coalition normally; one character cannot head both groups. Save the outgoing ruler and heir and prepare both offices before the transfer. If the handover removes the intended minister from play, use the prepared cabinet fallback without repeating the enthronement. Neither house changes personal faith.
- **The rites:** A settled Confucian court can present the ancestral rites as public ceremonies. Mahayana delegates can attend under their own patronage. Under Christianity the Zhu can keep them as dynastic ceremonies without requiring church participation. If faith is undecided, defer that description to the faith settlement; the charter does not convert the court, monarch, or cabinet.
- **After ratification:** Use **Southern Ming** while a Zhu crown or its native regency and a qualifying constitutional Monarchy are in force. Apply [The Southern Court Reborn’s aftermath](outcome-modifiers.md#the-southern-court-reborn) on completion. Use a persistent constitutional decision and status text to represent the Zheng First Minister as head of government; use vanilla ruler, government composition, and votes for actual authority. If the minister dies, leaves the country, loses the group leadership, or his bloc leaves government, mark the office vacant. Allow a new appointment only when the more powerful eligible bloc, measured as at the founding, is in government. Do not reshuffle a serving minister on a routine clout change. If the laws or crown cease to qualify, suspend the charter name and appointments without repeating the enthronement or reward. Territorial loss after the settlement does not automatically dethrone the Zhu. No land transfers; the [capital audiences](07-reunification-of-china.md#where-the-government-sits) decide where the court sits.

### A Mandate of Our Own — Zheng dynasty

- **Requires:** Monarchy and Appointed or Elected Bureaucrats.
- **Requires:** At least three Government Administration levels in Tungning’s Taiwan and legitimacy of at least 60.
- **Succession:** Confirm the crown with a living Zheng monarch. If there is a Zheng heir but another monarch reigns, wait for succession. If there is no eligible Zheng heir, offer a fictional Zheng cadet once without removing the incumbent.
- **Effects:** Display **Kingdom of Tungning** and apply [A Mandate of Our Own’s aftermath](outcome-modifiers.md#a-mandate-of-our-own) on completion.
- **Limits:** Grant no mainland claims and leave the Ming lock in place.

## Static checks

- Verify both opening routes, including a pending Qing offer and the end of mobilization. Check that endorsements and petitions respect the permanent Ming lock and the temporary cap.
- Verify simultaneous thresholds, falling below the threshold before ratification, and all three follow-ups. Check that losing a requirement resets the streak and that rewards apply once.
- Trace the Ming tiers with a treaty-port enclave, a chartered inland region, and loss or occupation of Taiwan. Trace competing faith nominations, each settled faith, a suspended debate, and a later law change. No nomination can alter the official religion or Devout.
- Verify Southern Passage success with a retained or lost grant, direct and subject rule over Manila, loss of Cebu or Manila, and a Philippine campaign after the original window. Neither southern bonus completes the Zheng follow-up on its own.
- Test both Zheng blocs as stronger, an equal-clout tie, the stronger group outside government, absence of the original candidates, a Zheng heir at restoration, and later cabinet vacancy. Confirm the Zhu native ruler and Zheng group leader are distinct and that a Zhu succeeds normally. Check law or dynasty changes without a second reward.
- Key cosmetic names to the outcome and current governing law. Keep the `TWG` tag and preserve existing treaties, religion, and unrelated laws on all routes.
- Vanilla references: `common/journal_entries/01_french_monarchism.txt`, `common/laws/00_governance_principles.txt`, and `common/dynamic_country_names/00_dynamic_country_names.txt`.
