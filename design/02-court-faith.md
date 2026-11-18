# The Faith of the Court

Tungning starts with a Catholic court and Freedom of Conscience (`common/scripted_effects/fh_tungning_setup.txt:37,68,123–133`). The debate concerns the court’s public faith. Its decision changes the state religion; religious laws and the faith of existing Pops are separate.

## Court balance

`fh_je_court_faith` begins at **60/100**. **0** restores an ancestral tradition; **100** embraces Christianity. A threshold commits on the same tick. At the fifth anniversary the nearer end is forced, with a tie preserving the current faith’s side; if the current state religion fits neither side, a tie goes to the ancestral side.

| Source | Change |
| --- | --- |
| An active Manila Compact or a Christian Devout in government | +1 per month each |
| A Confucian or Mahayana Devout in government; or State Religion with a Confucian or Mahayana state religion | −1 per month each |
| **Hear the Missions**: favors a nominated Catholic or Protestant settlement, with eligibility below | +12 |
| **Consult the Academies and Temples**: favors a nominated Confucian or Mahayana settlement, with eligibility below | −12 |

Use the Devout leader’s faith to identify the governing Devout, independently from the state religion. The church law and current religious population shape event eligibility. No passive law bonus comes from Freedom of Conscience or Total Separation alone.

Each side has two public nominations, usable while its bar is unresolved. A nomination records that side’s preferred faith, takes its ±12 action, and gives the named supporter +2 approval for six months. All four nominations share a six-month cooldown. The cadence makes a sustained ancestral campaign viable even with the Manila Compact in force. Protestant petitions can come from Reformers or Market Liberals in government, or from governing Intelligentsia under Freedom of Conscience or Total Separation if Taiwan has a university. Mahayana petitions can come from Traditionalists in government or a Mahayana share of at least 10% in Taiwan. Catholic nominations can come from the Devout or a live Manila Compact; Confucian nominations can come from Traditionalists or governing Landowners. Where there is only an external or popular sponsor, skip IG approval. Eligibility limits the action, not a previously valid recorded nomination.

At a threshold, adopt the nominated faith for that side immediately. If there is none, preserve the current faith when it belongs to the winning side; otherwise use **Catholic** or **Confucian**, respectively. The bar and event tooltips show what settlement will occur.

Each quarter, roll a 20% chance to draw one eligible event: a mission-school dispute under Freedom of Conscience with at least 3% Catholic population in Taiwan, an appeal from academies under State Religion, or a petition for a civil oath under Total Separation. Choices move the bar by 4 points; the civil oath can instead reduce Devout approval by 1 for a year and leave the bar still. An event starts a 12-month event cooldown, expires without effect if unanswered, and loses any ability to change the bar once the court settles.

## Denominations

| Settlement | Political base and three-year effect |
| --- | --- |
| **Catholic** (`rel:catholic`) | Catholic Devout +2 approval; Taiwan trade capacity +5%. Improve relations with Spain and the Philippines by 10 each, if alive; existing accords continue. |
| **Protestant** (`rel:protestant`) | Reformers/Market Liberals in government +2 approval, Catholic Devout −2; technology spread +5%. Spain and the Philippines each lose 10 relations if alive. |
| **Confucian** (`rel:confucian`) | Traditionalists in government +2 approval, Christian Devout −2; bureaucracy +5%. Spain and the Philippines each lose 10 relations if alive. |
| **Mahayana Buddhist** (`rel:mahayana`) | Mahayana Devout +2 approval, Christian Devout −2; +5% workforce qualifications in Taiwan. Spain and the Philippines each lose 10 relations if alive. |

Apply approval only if the described group or leader exists; evaluate at settlement, using pre-settlement supporter scopes so a religious change cannot misidentify the opposition. Existing treaty terms remain enforceable; the event affects goodwill, not the validity of the signed Manila Compact. A later clerical law change remains legal and does not restart the journal. Verify the two defaults, all four mapped religion keys, simultaneous claims/faith resolutions, and that changes to religion do not rewrite laws or convert Pops. Vanilla: `common/religions/religion.txt:1–7,65–83`, `events/bic_breakup.txt:105–117`, and `common/laws/00_church_and_state.txt:5,473,563`.
