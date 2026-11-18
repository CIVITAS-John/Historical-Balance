# Who Shall Rule the Eastern Sea?

The mainland question decides what Tungning claims. This journal decides who governs it. Ratify one route per campaign to open its follow-up.

## Opening

- **Entry:** `fh_je_constitutional_settlement`.
- **Requires:** `mainland_settled`. A pending Qing offer does not qualify.
- **Display:** Show all three bars. After final renunciation, show the Ming bar at zero and explain the permanent lock.
- **Subjects:** The Republic and Zheng routes are available to a Qing tributary. A constitutional change does not end the relationship or remove other subject restrictions.

## Mandates

### Republic

- **Starts at:** 15.
- **Monthly drift:** +1 if a Radical or Reformer leads the governing Intelligentsia or Trade Unions; +1 under Census Voting or Universal Suffrage.
- **Action:** **Convene a Civic Congress** (+10) with backing from the governing Intelligentsia or Trade Unions.

### Ming restoration

- **Starts at:** 25 if Tungning retained the claim.
- **Monthly drift:** +1 with a Traditionalist or Royalist in government; +1 while Tungning holds a qualifying foothold.
- **Action:** **Invite the Zhu Court** (+10) with backing from the governing Landowners or Devout.
- **Requires for invitation and ratification:** Independence and current ownership under the [mainland foothold rule](01-mainland-claim.md#mainland-foothold). An open reconquest journal by itself does not qualify.
- **Cap:** Until both conditions are met, cap the score at 75 and explain what is missing.

### Zheng dynasty

- **Starts at:** 35.
- **Monthly drift:** +1 under Monarchy with legitimacy of at least 60; +1 if the Armed Forces are in government.
- **Action:** **Petition for a Zheng Mandate** (+10) with backing from the governing Armed Forces or Landowners.

## Actions and ratification

- **Cooldown:** All three actions share 12 months.
- **Other effects:** Each action deducts 5 from both rival scores, to a minimum of zero. Record the last explicit endorsement.
- **Threshold:** Apply monthly drift as a batch. A score of 100 unlocks its **Ratify** action. There is no forced choice; all eligible tracks at 100 remain selectable.
- **Recommendation:** If several tracks are ready, highlight the most recently endorsed among them. If none has an endorsement, use the highest score before capping, then break ties in this order: Zheng, Republic, Ming.
- **Selection:** Recheck eligibility, record the chosen route, and open its follow-up.
- **AI:** Ratify an eligible track that fits current government and laws. Do not wait for a blocked Ming route.

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

## Integration and static checks

- Use native law and legitimacy checks, the shared ownership rule, one activation marker per route, and a counter for consecutive qualifying months.
- Grant completion modifiers and dynasty effects once. Allow subsequent law changes.
- Add cosmetic names keyed to the outcome and current governing law. Keep the `TWG` tag and leave other countries’ flags and names alone.
- Verify the opening lock, including while a Qing offer is pending. Check permanent Ming lock after renunciation and the temporary cap without independence or a foothold.
- Verify simultaneous thresholds, delayed ratification, and all three follow-ups. Check that a change of government, overlord, or ownership resets the streak where applicable and leaves treaties and unrelated laws intact.
- Vanilla references: `common/journal_entries/01_french_monarchism.txt`, `common/laws/00_governance_principles.txt`, and `common/dynamic_country_names/00_dynamic_country_names.txt`.
