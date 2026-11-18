# The Faith of the Court

Tungning starts Catholic, under Freedom of Conscience (`common/scripted_effects/fh_tungning_setup.txt`, lines 37 and 68). This debate sets the court’s public faith. It changes the state religion without changing religious laws or converting Pops.

## Court balance

- **Entry:** `fh_je_court_faith`, starting at **60/100**.
- **Endpoints:** **0** restores an ancestral tradition; **100** embraces Christianity. Resolve as soon as the balance reaches either end.
- **Deadline:** On the fifth anniversary, choose the nearer endpoint. A tie favors the current state religion’s side. If it fits neither side, choose the ancestral side.
- **Monthly drift:**
  - +1 while the Manila Compact is active.
  - +1 while a Christian leads the Devout and they are in government.
  - −1 while a Confucian or Mahayana Buddhist leads the Devout and they are in government.
  - −1 under State Religion if the state religion is Confucian or Mahayana Buddhist.
- **Scope:** Check the Devout leader’s faith separately from the state religion. Freedom of Conscience and Total Separation give no drift by themselves.

## Nominations

- **Availability:** Until the court settles. All four options share a six-month cooldown.
- **Effects:** Record the nominated faith for its side and give the named supporter +2 approval for six months. Skip approval if the only sponsor is external or popular.
- **Persistence:** A nomination remains valid if its sponsor later stops qualifying.

- **Hear the Missions** (+12)
  - **Catholic:** Requires the Devout or an active Manila Compact.
  - **Protestant:** Requires a Reformer or Market Liberal in government, or all three of the following: governing Intelligentsia, a university in Taiwan, and Freedom of Conscience or Total Separation.
- **Consult the Academies and Temples** (−12)
  - **Confucian:** Requires a Traditionalist or governing Landowners.
  - **Mahayana Buddhist:** Requires a Traditionalist in government or a Mahayana Buddhist share of at least 10% in Taiwan.

## Court events

- **Roll:** Each quarter, a 20% chance to draw one eligible event.
- **Mission-school dispute:** Freedom of Conscience and at least 3% Catholic population in Taiwan.
- **Academy appeal:** State Religion.
- **Civil oath petition:** Total Separation.
- **Effects:** Each event offers a choice between +4 and −4. The civil oath can instead leave the bar unchanged and give the Devout −1 approval for one year.
- **Cooldown and expiry:** Each event starts a 12-month cooldown. Unanswered events expire without effect; once the court settles, events cannot move the bar.

## Settlement

- Adopt the winning side’s last nomination. Without a nomination, keep the current faith if it belongs to that side. Otherwise default to **Catholic** or **Confucian**, respectively.
- Show the expected settlement in bar and event tooltips.
- Identify approval recipients before changing the state religion. Skip a recipient if the group or leader does not exist.
- Apply the approval and domestic effects below for three years. Apply relation changes once, to Spain and the Philippines separately if they still exist.
- Keep existing treaties, including the Manila Compact. A later religious law change does not restart the journal.

### Catholic (`rel:catholic`)

- Catholic Devout: +2 approval.
- Taiwan: +5% trade capacity.
- Spain and the Philippines: +10 relations each.

### Protestant (`rel:protestant`)

- Governing Reformers or Market Liberals: +2 approval.
- Catholic Devout: −2 approval.
- Tungning: +5% technology spread.
- Spain and the Philippines: −10 relations each.

### Confucian (`rel:confucian`)

- Governing Traditionalists: +2 approval.
- Christian Devout: −2 approval.
- Tungning: +5% bureaucracy.
- Spain and the Philippines: −10 relations each.

### Mahayana Buddhist (`rel:mahayana`)

- Mahayana Devout: +2 approval.
- Christian Devout: −2 approval.
- Taiwan: +5% workforce qualifications.
- Spain and the Philippines: −10 relations each.

## Static checks

- Verify the two defaults, all four religion keys, and simultaneous settlement of the claim and faith debates.
- Check that settlement leaves religious laws, Pops, and treaty terms unchanged.
- Vanilla references: `common/religions/religion.txt`, `events/bic_breakup.txt`, and `common/laws/00_church_and_state.txt`.
