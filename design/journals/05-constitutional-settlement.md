# Who Shall Rule the Eastern Sea?

Once the mainland settlement is complete, the court can build a mandate for a republic, a restored Ming court, or continued Zheng rule. Ratifying a mandate opens a follow-up to put it into effect.

## Opening

- **Entry:** `fh_je_constitutional_settlement`.
- **Requires:** Final renunciation, with or without a Qing deal, or reassertion followed by the [end of mobilization](06-mainland-reconquest.md#mobilization-after-reassertion). Neither a pending Qing offer nor an active mobilization opens the debate.
- **Display:** Show all three bars. After final renunciation, show the Ming bar at zero and explain the permanent lock.
- **Subjects:** The Republic and Zheng routes are available to a Qing tributary. A constitutional change does not end the relationship or remove other subject restrictions.

## Mandates

Each mandate runs from **0 to 200**. Sum monthly drift before applying it. Apply the caps after every change, including when Ming eligibility changes.

### Republic

- **Starts at:** 30.
- **Monthly drift:** +1 if a Radical or Reformer leads the governing Intelligentsia or Trade Unions; +1 under Census Voting or Universal Suffrage; −1 under Autocracy.
- **Action:** **Convene a Civic Congress** with backing from the governing Intelligentsia or Trade Unions. The Landowners take the approval penalty.

### Ming restoration

- **Starts at:** 50 after reassertion; locked at zero after renunciation.
- **Monthly drift:** +1 if a Traditionalist or Royalist leads a governing group; +1 while Tungning holds a qualifying foothold; −1 while Tungning is a subject.
- **Action:** **Invite the Zhu Court** with backing from the governing Landowners or Devout. The Industrialists take the approval penalty.
- **Requires for invitation and ratification:** Independence and current ownership under the [mainland foothold rule](01-mainland-claim.md#mainland-foothold). An open reconquest journal by itself does not qualify.
- **Cap:** While either condition is missing, cap the mandate at 150 and explain what is missing.

### Zheng dynasty

- **Starts at:** 70.
- **Monthly drift:** +1 under Monarchy with legitimacy of at least 60; +1 while the Armed Forces are in government; −1 under a Presidential or Parliamentary Republic.
- **Action:** **Petition for a Zheng Mandate** with backing from the governing Armed Forces or Landowners. The Intelligentsia take the approval penalty.

## Endorsements

All three actions share a six-month cooldown. Add 12 to the chosen mandate and subtract 5 from each rival. For six months, give the supporter +2 approval and the named opponent −2. If both possible supporters qualify, use the first listed. Record the last explicit endorsement.

## Court events

Each quarter, roll a 10% chance to draw one eligible petition. Petitions share a 12-month cooldown. Backing a petition adds 5 to its mandate and gives the petitioning group +1 approval for six months; rejecting it subtracts 5 and gives that group −1. Neither option counts as an endorsement. Recheck eligibility before applying either choice.

| Petition | Eligible while | Approval group |
| --- | --- | --- |
| Civic delegates | Census Voting or Universal Suffrage | Intelligentsia |
| Zhu envoys | Tungning reasserted the claim and is independent with a foothold | Landowners |
| Zheng officers | Armed Forces in government | Armed Forces |

## Ratification

- **Threshold:** A mandate at 200 unlocks its **Ratify** action while it remains eligible. There is no forced choice or deadline.
- **Recommendation:** If several mandates are ready, highlight the last explicit endorsement if it is ready. Otherwise prefer Zheng, then Republic, then Ming.
- **Selection:** Recheck the mandate and its requirements, record the route, and open its follow-up once. The AI favors an eligible route whose follow-up fits its laws, government, and holdings.

## Follow-up journals

For each route, maintain the listed ongoing requirements for six consecutive months. Reset the streak when any of them fails. Recheck eligibility before granting one-time completion effects.

### The Taiwan Convention — Republic

- **Requires:** Parliamentary Republic or Presidential Republic enacted through normal law play.
- **Requires:** Wealth Voting, Census Voting, or Universal Suffrage.
- **Requires:** Legitimacy of at least 60.
- **Effects:** Display **Republic of Tungning** while a valid republican law is active. Grant +5 base legitimacy for five years.
- **Continuity:** Keep the same playable country, subjects, treaties, religion, and surviving claims.

### The Southern Court Reborn — Ming restoration

- **Requires:** Independence, Monarchy, the current mainland foothold, and legitimacy of at least 60.
- **If a requirement is lost:** Pause the journal and reset the streak.
- **Enthronement:** Enthrone the living Zhu claimant already selected, or use one scripted fictional claimant if none exists.
- **Effects:** Display **Southern Ming** and grant +10 prestige for five years. Transfer no land and leave the capital in place.

### A Mandate of Our Own — Zheng dynasty

- **Requires:** Monarchy and Appointed or Elected Bureaucrats.
- **Requires:** At least three Government Administration levels in Tungning’s Taiwan and legitimacy of at least 60.
- **Succession:** Confirm the crown with a living Zheng monarch. If there is a Zheng heir but another monarch reigns, wait for succession. If there is no eligible Zheng heir, offer a fictional Zheng cadet once without removing the incumbent.
- **Effects:** Display **Kingdom of Tungning** and grant +5 base legitimacy and +5% bureaucracy for five years.
- **Limits:** Grant no mainland claims and leave the Ming lock in place.

## Static checks

- Verify both opening routes, including a pending Qing offer and the end of mobilization. Check that endorsements and petitions respect the permanent Ming lock and the temporary cap.
- Verify simultaneous thresholds, falling below the threshold before ratification, and all three follow-ups. Check that losing a requirement resets the streak and that rewards apply once.
- Key cosmetic names to the outcome and current governing law. Keep the `TWG` tag and preserve existing treaties, religion, and unrelated laws on all routes.
- Vanilla references: `common/journal_entries/01_french_monarchism.txt`, `common/laws/00_governance_principles.txt`, and `common/dynamic_country_names/00_dynamic_country_names.txt`.
