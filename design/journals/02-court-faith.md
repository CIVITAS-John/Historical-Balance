# The Faith of the Court

The Zheng court embraced Catholicism to secure Manila’s help. In 1836 Tungning is still officially Catholic and has Freedom of Conscience. The court can keep its Christian ties or return to an ancestral tradition.

The opening audience introduces Xu Wenjing, a Catholic scholar of the Confucian classics; Father Luo Jingde, who leads the Catholic Missions (Devout); and Samuel Talavan, who speaks for Sinkan’s Protestant congregations. Luo wants the missions to bring in Western textbooks and doctors; Xu wants their teachers and translations available to students beyond the mission schools. Estate tutors defend the old examinations.

## Opening effects

- **Conversions on hold:** Apply **−75% conversion speed** in Tungning’s states while the debate is open. Existing Catholic status alone does not ease the restriction.
- **Catholic preference:** If Catholicism is the latest faith explicitly nominated, ease the penalty to **−35%**. A new nomination for any other faith restores the full penalty. This does not change which nomination each side would adopt on winning.
- **Ends:** Remove the penalty when the court settles. Apply it only in states Tungning owns; ordinary laws still determine who can convert.

## Court balance

- **Entry:** `fh_je_court_faith`, starting at **120/200**.
- **Endpoints:** **0** restores an ancestral tradition; **200** endorses Christianity. Check after each action, event choice, or monthly drift.
- **Deadline:** On the tenth anniversary, choose the nearer endpoint. At **100**, favor the current state religion’s side; if it belongs to neither side, favor the ancestral side.
- **State Atheism:** While this law is active, suspend actions, drift, conversion restrictions, and settlement. On repeal, restore the debate and run any overdue deadline check. The journal never overrides the law’s religion.
- **Monthly drift:** Add all applicable effects:
  - +1 while the Manila Compact with Spain is active.
  - +1 while the Catholic Missions are in government.
  - +1 under State Religion if the official faith is Christian.
  - −1 if the Ming Estates are in government or another governing group has a Traditionalist leader. Count this once.
  - −1 under State Religion if the official faith is Confucian or Mahayana Buddhist.
  - −1 while Tungning is a direct tributary of a Confucian Qing.

Use religious heritage where the drift checks the official faith. A nomination changes the bar and the proposed outcome only. The Catholic Missions retain their name, traits, and constituency throughout the debate. The court can settle only on one of the four faiths below.

## Court actions

The four nominations share a six-month cooldown. Give the qualifying domestic sponsor with the most clout +2 approval and the listed opponent −2 for six months. Break ties in a fixed order; skip an absent group or an opponent who is also the sponsor. Record each nomination before moving the bar and keep it if the sponsor later stops qualifying.

| Nominate | Backing | Opposition |
| --- | --- | --- |
| Catholic | Governing Catholic Missions, or the active Manila Compact | Ming Estates |
| Protestant | A governing Reformer or Market Liberal; or the governing School of Practical Learning with a Taiwan university and either Freedom of Conscience or Total Separation | Catholic Missions |
| Confucian | Governing Ming Estates or a governing Traditionalist | Catholic Missions |
| Mahayana Buddhist | A governing Traditionalist or at least 10% Mahayana Buddhist population in Tungning’s Taiwan | Catholic Missions |

- **Hear the Missions** adds **+12** and nominates Catholicism or Protestantism. For six months, Taiwan gains 5 percentage points of education access and Tungning loses 5% bureaucracy to oversight of mission schools.
- **Consult the Academies and Temples** adds **−12** and nominates Confucianism or Mahayana Buddhism. For six months, Tungning gains 5% bureaucracy from local academies and loses 5% technology spread.
- The Manila Compact or the Buddhist population can sponsor a nomination without a domestic group.

## Court events

Roll a **10%** chance each quarter to draw one eligible event, then start a shared 12-month cooldown. Responses move the bar without replacing a nomination. Their modifiers last six months. Recheck eligibility on response and discard the event after 30 days or when the court settles.

| Event and trigger | +5 toward Christianity | −5 toward ancestral traditions |
| --- | --- | --- |
| **Mission-school dispute:** Freedom of Conscience and at least 3% Catholic population in Taiwan. Luo petitions for classrooms; Xu argues that mission pupils should also study the classics. | Open mission classrooms (Taiwan education access +3 percentage points) | Fund classical tutors (Taiwan qualifications +3%) |
| **A chaplain from Manila:** Active Manila Compact. Luo welcomes the visiting chaplain. | Receive the chaplain (Taiwan trade advantage +3%) | Send a secular delegation (influence +3%) |
| **The printing house:** A Taiwan university under either Freedom of Conscience or Total Separation. Talavan brings Siraya readers to the university press; Xu makes the case for printing them. | Print translations for the missions (technology spread +3%) | Print classical readers (Taiwan qualifications +3%) |
| **The academy’s appeal:** Governing Landowners or State Religion | Admit mission graduates to exams (Taiwan qualifications +3%) | Keep the classical examinations (bureaucracy +3%) |
| **A temple school endowment:** At least 10% Mahayana Buddhist population in Taiwan | Invite missions to match the endowment (Taiwan education access +3 percentage points) | Recognize temple schools (Taiwan qualifications +3%) |
| **The civil oath:** Total Separation | Permit a voluntary Christian blessing (influence +3%) | Permit voluntary ancestral rites (authority +3%) |

Apply Taiwan conditions and modifiers to the state Tungning actually owns; skip local effects if it no longer owns a state there.

Find the named speakers by their character templates, as in the opening audience. Use them only if they are alive and still in Tungning. If a speaker is unavailable, use an unnamed priest, scholar, or congregation delegate. The figures do not change event eligibility or count as nomination sponsors on their own.

## Settlement

Adopt the winning side’s latest nomination. Without one, keep the current state religion if it is one of that side’s two choices. Otherwise use **Catholicism** or **Confucianism**, respectively. Show the likely faith in the journal and before a settling choice.

Resolve the endpoint or deadline in one handler. Record the outcome and close the debate before applying the effects. Set the official faith once if it differs; only now update the [Devout name and traits](README.md#interest-groups) and recalculate Pop support. If the incumbent Devout leader’s personal faith does not match the result, appoint a living representative of the new faith from Tungning’s Devout, or create a matching delegate if needed. A Sinkan pastor can represent the Reformed congregations; Talavan remains a schoolmaster. Luo and other incumbents keep their personal faiths and may leave the leadership without being expelled. Ordinary succession resumes afterward.

Use the groups and leaders present before the change to identify the sponsors; if the Catholic Missions are displaced, express their opposition as **+10% radicals from political movements in Tungning’s Taiwan for one year** if they were not marginalized, rather than giving the incoming Devout their disapproval. The outcome does not change laws, directly convert Pops, or rewrite treaties. Apply approval and domestic effects for three years and relations once to each surviving partner.

[Taiping negotiations](08-taiping-rebellion.md#bargain-with-the-heavenly-kingdom) use the current official faith even while this debate is open. A nomination has no diplomatic effect before settlement.

| Faith | Approval | Domestic effect | Relations with Spain and the Philippines |
| --- | --- | --- | --- |
| Catholic (`rel:catholic`) | Catholic Missions +2 | Taiwan: +5% trade advantage | +10 each |
| Protestant (`rel:protestant`) | Reformed Congregations +2; governing Reformers or Market Liberals +2 | Tungning: +5% technology spread | −10 each |
| Confucian (`rel:confucian`) | Ritual Academies +2; governing Ming Estates or governing Traditionalists +2 | Tungning: +5% bureaucracy | −10 each |
| Mahayana Buddhist (`rel:mahayana`) | Buddhist Temples +2 | Taiwan: +5% qualifications | −10 each |

Where several groups qualify for the same approval in the table, use the highest clout and a fixed order for ties. Apply the approval only once to the Devout even if they also meet a sponsor condition.

## Static checks

- Trace both endpoints, a deadline tie, the two defaults, and each nominated faith. Include a sponsor leaving government and an event expiring after settlement.
- Check conversion at opening, after a Catholic nomination, after a different nomination, and after settlement. State transfers must not leave the penalty with another country.
- Show the Catholic Missions after each nomination and a suspended deadline, then check the correct name, leader, traits, and recalculated support after all four outcomes. Trace an unavailable Luo, an already matching incumbent, and a pending event after settlement. Keep other countries’ Devout unchanged.
- Check that the Spanish compact and Qing tributary terms alter drift only while active. The faith journal runs alongside the mainland debate and can settle independently of it.
- Verify that settlement leaves laws, Pops, and the Manila Compact intact. Ordinary law effects still apply under the new state religion.
- References: `common/scripted_effects/fh_tungning_setup.txt` and `common/scripted_effects/fh_tungning_diplomacy.txt`; vanilla `common/religions/religion.txt`, `common/laws/00_church_and_state.txt`, `common/modifier_type_definitions/00_modifier_types.txt`, `common/journal_entries/07_japanese_religion.txt` (local faith shares), and `events/bic_breakup.txt` (state religion changes).
