# The Faith of the Court

The Zheng court embraced Catholicism to secure Manila’s help. Zheng Kezang invoked a promise made in the name of the Southern Ming’s Yongli court while the Zhu princes kept their ancestral rites. In 1836 Tungning is still officially Catholic. Its **Yongli Articles of Conscience** preserve the protections once sought for Catholics and extend them to other congregations. The court must decide both which faith to profess and which protections to keep.

The opening audience introduces Xu Wenjing, a Catholic scholar of the Confucian classics; Father Luo Jingde, who leads the Catholic Missions (Devout); and Samuel Talavan, who speaks for Sinkan’s Protestant congregations. Luo wants the missions to bring in Western textbooks and doctors; Xu wants their teachers and translations available to students beyond the mission schools. Estate tutors defend the old examinations.

## Opening effects

- **Yongli Articles:** Start with the [Yongli amendment to Freedom of Conscience](../law-plan.md#laws-against-vanilla). Its −50% conversion speed continues while the amendment is in force.
- **School charter:** Level 1 Religious Schools starts with the Tungning School Charter, which cancels the school conversion bonus. While Religious Schools remains active, it still blocks the Total Separation settlement.
- **Church law on hold:** Block voluntary and imposed enactment in the Church and State law group, and block repeal of the Articles, until settlement or interruption. This applies to the same founding country if it restores the Ming; restoration neither ends nor restarts the debate. Keep other law groups available.
- **Conversions on hold:** While the debate is open, add a temporary **−25% conversion speed** in Tungning’s states, for **−75%** from the journal and Articles together. Existing Catholic status alone does not ease the restriction.
- **Catholic preference:** If Catholicism is the latest faith explicitly nominated, use a temporary **+15% conversion speed** instead, for **−35%** from the journal and Articles together. A new nomination for any other faith restores the full penalty. This does not change which nomination each side would adopt on winning.
- **Ends:** Remove the journal’s temporary conversion modifier when the court settles or the debate is interrupted. Apply it only in states Tungning owns; ordinary laws still determine who can convert.

## Court balance

- **Entry:** `fh_je_court_faith`, starting at **120/200** after the Articles are in place at the 1836 opening.
- **Endpoints:** **0** restores an ancestral tradition; **200** endorses Christianity. Check after each action, event choice, or monthly drift.
- **Deadline:** On the tenth anniversary, choose the nearer endpoint. At **100**, favor the current state religion’s side; if it belongs to neither side, favor the ancestral side.
- **Interruption:** If a forced regime change or external script replaces Freedom of Conscience or removes the Articles, close without a settlement. Cancel pending choices and clear the lock and temporary conversion modifier. Keep the resulting law and faith and apply only the [interruption aftermath](outcome-modifiers.md#court-faith).
- **Monthly drift:** Add all applicable effects:
  - +1 while the Manila Compact with Spain is active.
  - +1 while the Catholic Missions are in government.
  - +1 while Tungning has a direct overlord whose state religion has Christian heritage.
  - −1 if the Ming Estates are in government or another governing group has a Traditionalist leader. Count this once.
  - −1 while Tungning has a direct overlord whose state religion does not have Christian heritage.
  - Add the Catholic and Protestant shares of Tungning’s Taiwan population and subtract the Confucian and Mahayana shares. A difference of 20 percentage points moves the bar by 0.20 that month. Other faiths are neutral, and the factor is zero if Tungning owns no part of Taiwan.

A nomination changes the bar and the proposed outcome only. The Catholic Missions retain their name, traits, and constituency until settlement. The court can settle only on one of the four faiths below.

## Court actions

The four nominations share a six-month cooldown. Give the qualifying domestic sponsor with the most clout +2 approval and the listed opponent −2 for six months. Break ties in a fixed order; skip an absent group or an opponent who is also the sponsor. Record each nomination before moving the bar and keep it if the sponsor later stops qualifying.

| Nominate | Backing | Opposition |
| --- | --- | --- |
| Catholic | Governing Catholic Missions, or the active Manila Compact | Ming Estates |
| Protestant | A governing Reformer or Market Liberal; or the governing School of Practical Learning with a Taiwan university | Catholic Missions |
| Confucian | Governing Ming Estates or a governing Traditionalist | Catholic Missions |
| Mahayana Buddhist | A governing Traditionalist or at least 10% Mahayana Buddhist population in Tungning’s Taiwan | Catholic Missions |

- **Hear the Missions** adds **+12** and nominates Catholicism or Protestantism. For six months, Taiwan gains 5 percentage points of education access and Tungning loses 5% bureaucracy to oversight of mission schools.
- **Consult the Academies and Temples** adds **−12** and nominates Confucianism or Mahayana Buddhism. For six months, Tungning gains 5% bureaucracy from local academies and loses 5% technology spread.
- The Manila Compact or the Buddhist population can sponsor a nomination without a domestic group.

## Court events

Roll a **10%** chance each quarter to draw one eligible event, then start a shared 12-month cooldown. Responses move the bar without replacing a nomination. The court can also let the matter rest without effect; this happens automatically if no response is chosen within 30 days. Recheck eligibility on response and discard pending events when the settlement audience opens.

When an option promotes a faith, it converts **0.5% of Taiwan Pops outside that faith** if the faith is unofficial. If it is already the state religion, the option instead adds **+25% conversion speed in Taiwan** for six months, ending early if the debate closes. This adds to the Articles and nomination modifiers; ordinary laws still govern natural conversion. Other event modifiers last six months unless the option specifies otherwise.

| Event and trigger | +5 toward Christianity | −5 toward ancestral traditions |
| --- | --- | --- |
| **Mission-school dispute:** At least 3% Catholic population in Taiwan. Luo petitions for classrooms; Xu argues that mission pupils should also study the classics. | Put the missions in charge (promote Catholicism; -2% radicals among Catholic Pops and +0.5% among other faiths in Taiwan; Taiwan education access +5 percentage points for one year) | Fund classical tutors (promote Confucianism; Taiwan qualifications +3%) |
| **A chaplain from Manila:** Active Manila Compact. Luo welcomes the visiting chaplain. | Receive the chaplain (promote Catholicism; Taiwan trade advantage +3%) | Send a secular delegation (influence +5%) |
| **The printing house:** A Taiwan university. Talavan brings Siraya readers to the university press; Xu makes the case for printing them. | Print translations for the missions (promote Protestantism; technology spread +5%) | Print classical readers (promote Confucianism; Taiwan qualifications +3%) |
| **The academy’s appeal:** Governing Ming Estates. | Admit mission graduates to exams (promote Catholicism; Taiwan qualifications +5%) | Keep the classical examinations (promote Confucianism; bureaucracy +3%) |
| **A temple school endowment:** At least 10% Mahayana Buddhist population in Taiwan. | Invite missions to match the endowment (promote Catholicism; Taiwan education access +3 percentage points) | Recognize temple schools (promote Mahayana Buddhism; Taiwan qualifications +3%) |
| **A visit to the Reformed congregations:** Tungning owns part of Taiwan and has an active, voluntarily signed treaty with a Protestant country. | Welcome Reformed teachers (promote Protestantism; +0.5% radicals among Catholic and Confucian Pops in Taiwan) | Keep the treaty to secular matters. |

Apply Taiwan conditions and modifiers to the state Tungning actually owns; skip local effects if it no longer owns a state there.

Find the named speakers by their character templates, as in the opening audience. Use them only if they are alive and still in Tungning. If a speaker is unavailable, use an unnamed priest, scholar, or congregation delegate. The figures do not change event eligibility or count as nomination sponsors on their own.

## Settlement

At either endpoint or the deadline, record the winning side’s latest nomination as the faith to adopt at settlement. Without one, use the current state religion if it is one of that side’s two choices. Otherwise use **Catholicism** or **Confucianism**, respectively. Show the likely faith in the journal.

Open a **30-day settlement audience** and freeze the bar, nominations, and court events. Keep the church law lock and temporary conversion modifier in place during the audience. Show the proposed faith and the [recognition, immediate effects, and duration](outcome-modifiers.md#court-faith) with each choice. Any of the four faiths can be paired with any legal choice below.

| Choice | Church law after settlement |
| --- | --- |
| **Keep the Articles** | Retain Freedom of Conscience and the Yongli amendment, including for Catholics if they are now outside the official faith. |
| **Repeal the Articles** | Remove only the Yongli amendment. Keep Freedom of Conscience and any other amendments on it. |
| **Establish the settled faith** | Remove the Articles and adopt vanilla **State Religion**, if legal. |
| **Separate church and state** | Remove the Articles and adopt vanilla **Total Separation**, if legal. Check Empiricism, Theocracy, religious power bloc leadership, and incompatible school laws. |

**Keep the Articles** is the timeout and the AI’s default when it has no strong reason to change. Show switches only when they meet native prerequisites apart from the journal lock. On response, recheck that the Articles are still in force. Guard the settlement against callbacks and lift the lock before rechecking native availability. If the requested switch is no longer legal, keep the Articles. An external replacement before settlement interrupts the audience.

Apply any church law change before setting the official faith. Leave unrelated enactments alone. Then update the [Devout name and traits](README.md#interest-groups) and recalculate Pop support. If the incumbent Devout leader’s personal faith does not match the result, appoint a living representative of the new faith from Tungning’s Devout, or create a matching delegate if needed. A Sinkan pastor can represent the Reformed congregations; Talavan remains a schoolmaster. Luo and other incumbents keep their personal faiths and may leave the leadership without being expelled. Ordinary succession resumes afterward.

If active Confucian Academies lose their required official faith, use the [school law fallback](../law-plan.md#laws-against-vanilla) and preserve investment where schools remain active. Record the actual law choice and adopted faith, conclude the journal, and apply the [faith aftermath](outcome-modifiers.md#court-faith) once. The settlement does not rewrite treaties.

[Taiping negotiations](08-taiping-rebellion.md#bargain-with-the-heavenly-kingdom) use the current official faith even while this debate is open. A nomination has no diplomatic effect before settlement.

Use `rel:catholic`, `rel:protestant`, `rel:confucian`, and `rel:mahayana` for the four possible official faiths.

## Static checks

- Trace both endpoints, a deadline tie, the two default faiths, and each nominated faith. Include a sponsor leaving government and a pending event when the audience opens.
- Check the combined conversion effects at opening, after each type of nomination, and during the audience. At settlement or interruption, remove the journal effect and retain the Articles’ effect only if the amendment remains. State transfers must not leave the journal effect with another country.
- Verify that neither ordinary enactment, imposed enactment, nor repeal can bypass the lock during debate or audience. Restore the Ming in both phases without resetting progress. Force a replacement law and confirm only the interruption aftermath applies, without a second law change.
- Trace Keep, Repeal, both eligible and blocked switches, and audience timeout. Exercise a choice that becomes illegal and verify it keeps the Articles. Settlement itself leaves the Manila Compact, Pop religions, and unrelated laws or enactments intact except for the school law fallback.
- Show the Catholic Missions throughout nominations and the audience, then check the Devout name, leader, traits, and support after all four faith outcomes. Trace an unavailable Luo and an already matching incumbent. Keep other countries’ Devout unchanged.
- Check drift with independent Tungning, direct Christian and non-Christian overlords, and no owned Taiwan state. Changing Taiwan’s religious makeup must change the monthly balance. The faith journal runs alongside the mainland debate and can settle independently of it.
- Trace both conversion branches, the quarterly draw, the shared cooldown and the 30-day response window. Check a Protestant partner on either side of a treaty and discard a visit if that treaty ends or the partner changes faith. Check loss of Taiwan before and after a response and a visit with Talavan unavailable.
- References: `common/scripted_effects/fh_tungning_setup.txt` and `common/scripted_effects/fh_tungning_diplomacy.txt`; vanilla `common/law_groups/00_laws.txt` (church law lock), `common/laws/00_church_and_state.txt` (eligibility), `common/amendments/00_amendments_ip5_04.txt` (amendment precedent), and `events/bic_breakup.txt` (state religion changes).
