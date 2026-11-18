# Who Shall Rule the Eastern Sea?

The mainland question decides what Tungning claims. This journal decides who governs it. Only one route is chosen per campaign; the winner opens a distinct follow-up with its own requirements.

## Three mandates

`fh_je_constitutional_settlement` appears only after `mainland_settled` is recorded. In particular, a human Qing offer still awaiting an answer does not unlock it. Show all three bars at once. A permanently blocked Ming bar is shown at zero with the mainland renunciation as its reason.

| Track | Starts at | Monthly movement | Action |
| --- | ---: | --- | --- |
| Republic | 15 | +1 if a Radical or Reformer leads a governing Intelligentsia or Trade Unions; +1 under Census Voting or Universal Suffrage | **Convene a Civic Congress** (+10), with the backing of the Intelligentsia or Trade Unions in government |
| Ming restoration | 25 if the claim was retained | +1 with a Traditionalist or Royalist in government; +1 after Tungning gains a qualifying mainland foothold | **Invite the Zhu Court** (+10), with governing Landowners or Devout support; available only while independent with a qualifying foothold |
| Zheng dynasty | 35 | +1 under Monarchy with legitimacy of at least 60; +1 if the Armed Forces are in government | **Petition for a Zheng Mandate** (+10), with the backing of the Armed Forces or Landowners in government |

The three actions share a 12-month cooldown and each subtracts 5 from the two rival scores, to a minimum of zero. Record the last explicit endorsement for tie breaking. A qualifying mainland foothold is full ownership of **one** of Fujian, Guangdong, or Zhejiang. Before Tungning has both the foothold and independence, a retained Ming track is capped at 75. The panel explains what is missing. The Republic and Zheng tracks remain available while a Qing tributary; constitutional change alone does not break tributary status or lift any other subject restrictions.

Apply monthly drift as a batch. A track at 100 unlocks its **Ratify** action; this debate has no forced endpoint. Players can leave other tracks ready while building toward a Ming restoration. If several are ready together, highlight the most recently endorsed among them; otherwise recommend the highest pre-clamp score, then Zheng, Republic, Ming. All eligible ready tracks remain selectable. Recheck eligibility and record the route as soon as a ratification action is pressed, before opening its follow-up. The AI ratifies an eligible ready track consistent with its current government and laws and does not wait for a blocked Ming route.

## Follow-up journals

### The Taiwan Convention — Republic

Enact Parliamentary Republic or Presidential Republic through normal law play, with Wealth Voting, Census Voting, or Universal Suffrage. Hold legitimacy of at least 60 for six consecutive months; dropping any requirement resets the streak. Completion adopts the name **Republic of Tungning** when a valid republican governing law is active. Reward the constitutional transition with +5 base legitimacy for five years. Tungning stays the same playable country and keeps its subjects, treaties, state religion, and any surviving claims.

### The Southern Court Reborn — Ming restoration

Maintain independence, Monarchy, and the foothold for six consecutive months with government legitimacy at least 60. On completion, enthrone a living, already selected Zhu claimant; if none exists, use one scripted fictional Zhu claimant. Change the displayed country name to **Southern Ming** and give +10 prestige for five years. Transfer no land and do not force a capital move. The journal waits if independence or the foothold is lost, and the streak resets; eligibility is rechecked immediately before enthronement.

### A Mandate of Our Own — Zheng dynasty

Keep or enact Monarchy, pass Appointed or Elected Bureaucrats, and maintain at least three Government Administration levels in Tungning’s Taiwan plus legitimacy of at least 60 for six consecutive months. Dropping a requirement resets the streak. Confirm the Zheng crown with a living Zheng monarch. If a Zheng member is available as heir but a different monarch rules, require succession before completion; if the house has no eligible heir, one guarded event offers a fictional Zheng cadet as heir without unseating the incumbent. Completion confirms the existing **Kingdom of Tungning** title and gives +5 base legitimacy and +5% bureaucracy for five years. This local mandate grants no new mainland claims and does not reopen the Ming route.

## Integration and verification

Use province ownership and the native law and legitimacy checks for progress, a per-route activation marker, and a consecutive-month counter reset by missing prerequisites. Grant completion modifiers and dynasty effects once; a subsequent law change remains legal. Apply cosmetic names using an additive dynamic-name file keyed by outcome and current governing law. Keep `TWG` as the tag; do not touch flags or names belonging to other countries.

Verify lock before mainland settlement (including a pending Qing offer), permanent Ming lock after renunciation, temporary Ming cap where a retained claim has no foothold, a simultaneous threshold, delaying ratification until another track is ready, and all three follow-ups. Verify that changing government form, an overlord, or ownership breaks the applicable streak and never deletes a valid treaty or rewrites civil or religious laws. Vanilla references: `common/journal_entries/01_french_monarchism.txt:29–31,54–56,128–146`, `common/laws/00_governance_principles.txt:337,487`, and `common/dynamic_country_names/00_dynamic_country_names.txt:3913–3964`.
