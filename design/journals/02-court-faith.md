# The Faith of the Court

The Zheng court embraced Catholicism to secure Manila’s help. In 1836 Tungning is still officially Catholic and has Freedom of Conscience. The court can keep its Christian ties or return to an ancestral tradition.

## Court balance

- **Entry:** `fh_je_court_faith`, starting at **120/200**.
- **Endpoints:** **0** restores an ancestral tradition; **200** endorses Christianity. Check after each action, event choice, or monthly drift.
- **Deadline:** On the tenth anniversary, choose the nearer endpoint. At **100**, favor the current state religion’s side; if it belongs to neither side, favor the ancestral side.
- **Monthly drift:** Add all applicable effects:
  - +1 while the Manila Compact with Spain is active.
  - +1 while the governing Devout have a Christian leader.
  - +1 under State Religion if the official faith is Christian.
  - −1 while the governing Devout have a Confucian or Mahayana Buddhist leader.
  - −1 while any governing group has a Traditionalist leader.
  - −1 under State Religion if the official faith is Confucian or Mahayana Buddhist.
  - −1 while Tungning is a direct tributary of a Confucian Qing.

Use religious heritage to identify Christian faiths and check the Devout leader separately from the state religion. The court can settle only on one of the four faiths below.

## Court actions

The four nominations share a six-month cooldown. Give the qualifying domestic sponsor with the most clout +2 approval and the listed opponent −2 for six months. Break ties in a fixed order; skip an absent group or an opponent who is also the sponsor. Record each nomination before moving the bar and keep it if the sponsor later stops qualifying.

| Nominate | Backing | Opposition |
| --- | --- | --- |
| Catholic | Governing Catholic Devout, or the active Manila Compact | Landowners |
| Protestant | A governing Reformer or Market Liberal; or governing Intelligentsia with a Taiwan university and either Freedom of Conscience or Total Separation | Catholic Devout |
| Confucian | Governing Landowners or a governing Traditionalist | Christian Devout |
| Mahayana Buddhist | A governing Traditionalist or at least 10% Mahayana Buddhist population in Tungning’s Taiwan | Christian Devout |

- **Hear the Missions** adds **+12** and nominates Catholicism or Protestantism. For six months, Taiwan gains 5 percentage points of education access and Tungning loses 5% bureaucracy to oversight of mission schools.
- **Consult the Academies and Temples** adds **−12** and nominates Confucianism or Mahayana Buddhism. For six months, Tungning gains 5% bureaucracy from local academies and loses 5% technology spread.
- The Manila Compact or the Buddhist population can sponsor a nomination without a domestic group.

## Court events

Roll a **10%** chance each quarter to draw one eligible event, then start a shared 12-month cooldown. Responses move the bar without replacing a nomination. Their modifiers last six months. Recheck eligibility on response and discard the event after 30 days or when the court settles.

| Event and trigger | +5 toward Christianity | −5 toward ancestral traditions |
| --- | --- | --- |
| **Mission-school dispute:** Freedom of Conscience and at least 3% Catholic population in Taiwan | Open mission classrooms (Taiwan education access +3 percentage points) | Fund classical tutors (Taiwan qualifications +3%) |
| **A chaplain from Manila:** Active Manila Compact | Receive the chaplain (Taiwan trade advantage +3%) | Send a secular delegation (influence +3%) |
| **The printing house:** A Taiwan university under either Freedom of Conscience or Total Separation | Print translations for the missions (technology spread +3%) | Print classical readers (Taiwan qualifications +3%) |
| **The academy’s appeal:** Governing Landowners or State Religion | Admit mission graduates to exams (Taiwan qualifications +3%) | Keep the classical examinations (bureaucracy +3%) |
| **A temple school endowment:** At least 10% Mahayana Buddhist population in Taiwan | Invite missions to match the endowment (Taiwan education access +3 percentage points) | Recognize temple schools (Taiwan qualifications +3%) |
| **The civil oath:** Total Separation | Permit a voluntary Christian blessing (influence +3%) | Permit voluntary ancestral rites (authority +3%) |

Apply Taiwan conditions and modifiers to the state Tungning actually owns; skip local effects if it no longer owns a state there.

## Settlement

Adopt the winning side’s latest nomination. Without one, keep the current state religion if it is one of that side’s two choices. Otherwise use **Catholicism** or **Confucianism**, respectively. Show the likely faith in the journal and before a settling choice.

The court changes the official faith once. It does not change laws, directly convert Pops, or rewrite treaties. Apply approval and domestic effects for three years, using interest group leaders as they were before the change. Apply relations once to each surviving partner.

| Faith | Approval | Domestic effect | Relations with Spain and the Philippines |
| --- | --- | --- | --- |
| Catholic (`rel:catholic`) | Catholic Devout +2 | Taiwan: +5% trade advantage | +10 each |
| Protestant (`rel:protestant`) | Governing Reformers or Market Liberals +2; Catholic Devout −2 | Tungning: +5% technology spread | −10 each |
| Confucian (`rel:confucian`) | Governing Traditionalists +2; Christian Devout −2 | Tungning: +5% bureaucracy | −10 each |
| Mahayana Buddhist (`rel:mahayana`) | Mahayana Devout +2; Christian Devout −2 | Taiwan: +5% qualifications | −10 each |

## Static checks

- Trace both endpoints, a deadline tie, the two defaults, and each nominated faith. Include a sponsor leaving government and an event expiring after settlement.
- Check that the Spanish compact and Qing tributary terms alter drift only while active. The faith journal runs alongside the mainland debate and can settle independently of it.
- Verify that settlement leaves laws, Pops, and the Manila Compact intact. Ordinary law effects still apply under the new state religion.
- References: `common/scripted_effects/fh_tungning_setup.txt` and `common/scripted_effects/fh_tungning_diplomacy.txt`; vanilla `common/religions/religion.txt`, `common/laws/00_church_and_state.txt`, `common/modifier_type_definitions/00_modifier_types.txt`, `common/journal_entries/07_japanese_religion.txt` (local faith shares), and `events/bic_breakup.txt` (state religion changes).
