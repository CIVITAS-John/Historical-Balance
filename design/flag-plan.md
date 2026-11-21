# Names and flags of the Zheng court

**Proposed design.** In 1836 the map reads **Tungning** and the country flies the old **鄭 command banner**. At home, the Zheng govern in the name of Great Ming until they renounce the claim or establish a new constitutional identity. The banner belongs to the Zheng house and survives renunciation. Forming **Ming** brings a separate set of flags based on its government and the seats it holds.

## Names at home and abroad

Use **the Zheng court** or **the court** in domestic narration. Use **Great Ming** (大明) in opening court records, invocations of the Yongli reign, and memorials that assert Ming allegiance. This is a claim to continuity; the opening Zheng ruler is no Zhu emperor. After renunciation, current state documents stop speaking for the Ming. The republic speaks in the name of its assembly, a restored Zhu crown speaks for Southern Ming, and a Zheng crown confirmed in its own right speaks for the Zheng house.

Use **Tungning** (東寧) in foreign correspondence, trade, and the map and diplomacy interface. Foreign governments need not all use that name: Qing can speak of Taiwan or the Zheng without recognizing them. **Kingdom of Tungning** and **Republic of Tungning** are foreign-facing styles. Victoria 3 exposes one country name at a time; use the speaker and audience to make the difference clear in events.

The [明鄭 article](https://zh.wikipedia.org/wiki/%E6%98%8E%E9%84%AD) records Great Ming as the polity’s name and identifies the Zheng banner. The [National Palace Museum’s study of Ming–Zheng artifacts](https://www.npm.gov.tw/NewChineseArtDownload.ashx?bid=3976) documents Ming allegiance and continued Yongli dating under Zheng Jing; it also records 東寧 as a place name. The foreign-only rule here concerns the name of the state in the alternate timeline.

## Tungning flags (`TWG`)

Within `TWG`, use the first matching row. Keep the native higher-priority flag rules and revolutionary marks.

| Priority | When | Flag |
| --- | --- | --- |
| 20 | The Southern Ming charter is active: the qualifying monarchy and voting law are in force, with a Zhu ruler or regency for a Zhu heir. | Existing Southern Ming sun and moon (`MIG_southern`). A vacant Zheng cabinet office does not suspend it. |
| 15 | The active law is Presidential or Parliamentary Republic, including a republic formed outside the Taiwan Convention. | Existing teal-and-white wheel (`TWG_republic`). The law already changes the flag; the named republican route supplies the foreign style **Republic of Tungning**. |
| 10 | **A Mandate of Our Own** is complete, a Zheng holds the crown or is heir under a regency, and the country’s scripted state religion is Catholic. | Existing red and gold cross (`TWG_catholic`). The court raises a standard associated with Manila to mark the Zheng crown’s own settlement. The cross yields to the old banner if the state faith changes while the Zheng crown remains. |
| 5 | An existing `TWG` has neither a monarchy nor a civic republic, or has a monarchy with no Zheng crown or Zheng regency and no active Zhu charter. | Existing blue and gold wheel, renamed `TWG_maritime`. It represents the ports and fleet without making a dynastic claim. |
| 1 | Opening government, another Zheng monarchy, or a preview without a live `TWG` country. | **Zheng command banner** (`TWG`): white field, dark red ring, and dark traditional **鄭**. |

Reassertion, renunciation, becoming a Qing tributary, a Taiping pact, or victories in the Southern Passage or Manila never switch the flag by themselves. A foothold, a capital move, and the [reunification proclamation](journals/07-reunification-of-china.md#proclaim-the-settlement) likewise leave the regime’s flag in place. Ratifying a mandate alone never switches the flag. If the Zhu charter is suspended, re-evaluate the table using the current regime; restoring the charter brings its banner back.

## Ming flags (`MIG`)

Use this table once a country [forms Ming](../common/country_formation/fh_ming_formation.txt#L1) through Nation Formation. Proclaiming reunification through the journal leaves the country’s existing tag and flag rules in place. The Zhu charter can fly the Southern Ming colors while still on `TWG`; forming `MIG` hands the choice to the national rules below, regardless of the founding court.

| Priority | When | Display name and flag |
| --- | --- | --- |
| 2100 | Council Republic. | **People’s Republic of Ming** — `MIG_council`, a gold star above a gold hammer and hoe on dark red. Its priority preserves this design over the generic communist flag. |
| 10 | A monarchy owns all of the Beijing state region. | **Great Ming** — `MIG_imperial`, gold dragon on a red field with gold trim. It wins even if Nanjing is also held. |
| 10 | A monarchy owns all of the Nanjing state region but does not own all of Beijing. | **Restored Ming** — `MIG_southern`, red sun and blue crescent on white with dark red trim. It shares the banner used by the Zhu charter on `TWG`, which displays **Southern Ming**. |
| 10 | Presidential or Parliamentary Republic. | **Republic of Ming** — `MIG_republic`, a blue and red bicolor with a white sun and crescent. Beijing and Nanjing do not affect the republican flag. |
| 1 | No Ming-specific rule above applies, including a monarchy without full ownership of either seat. | **Ming** — `MIG`, yellow sun and white crescent on red; higher priority native rules still apply, including the generic anarchist flag. |

These are the mod’s existing designs. Keep the [Ming flag definitions](../common/flag_definitions/fh_ming_flags.txt#L1), [artwork](../common/coat_of_arms/coat_of_arms/fh_ming_coa.txt#L1), [identity checks](../common/scripted_triggers/fh_country_identity.txt#L19), and [names](../common/dynamic_country_names/fh_country_names.txt#L34) together. The two court variants depend on present ownership, not the capital’s location, military occupation, or subject holdings. Losing Beijing under a monarchy drops the dragon; the restored banner takes over if Nanjing is still wholly owned, otherwise the plain Ming banner applies. Keep the existing matching subject cantons and let the Nation Formation preview evaluate the prospective founder’s laws and territory as it does today.

## Implementation

1. **Draw the banner.** Use the [exact artwork in the linked infobox](https://commons.wikimedia.org/wiki/File:Flag_of_Ming_Cheng.svg) as a reference for an original game asset. Call it a reconstruction of the Zheng command banner: the SVG is modern, and [Albert Herport’s eyewitness account of the Zheng troops’ banners](https://ildsc.yuntech.edu.tw/23-dec-2022-%E8%8D%B7%E8%98%AD%E6%99%82%E6%9C%9F%E9%84%AD%E6%88%90%E5%8A%9F%E8%BB%8D%E6%97%97/) describes several styles. Use a white solid pattern, try `ce_frame_circle_outline.dds` for the ring, and add a custom glyph texture at `gfx/coat_of_arms/colored_emblems/ce_fh_zheng.dds`. Keep the circle and the 鄭 character legible at map and canton size; record the visual source with the asset.
2. **Apply the precedence.** In [the TWG coats of arms](../common/coat_of_arms/coat_of_arms/fh_tungning_coa.txt#L1), move the old blue wheel to `TWG_maritime` and make `TWG` the command banner. In [the TWG flag list](../common/flag_definitions/fh_tungning_flags.txt#L1), give each row the matching `subject_canton` for subjects whose own definition allows one. Keep the historical baseline unconditional. For the other rows, require `exists = scope:target` before reading `scope:actor` so previews do not inherit the releasing player’s regime. Skip the variants when `fh_tungning_history_started` is set but `fh_tungning_bootstrapped` is missing, using the existing [setup markers](../common/scripted_effects/fh_tungning_setup.txt#L11). Keep the native rules for an overlord’s canton.
3. **Share the live identity checks.** Keep `fh_has_southern_ming_charter` and `fh_has_civic_republic` from [the identity triggers](../common/scripted_triggers/fh_country_identity.txt#L8). Add a presentation check for a Zheng monarch, including a regency for a Zheng heir, using the existing [Zheng character check](../common/scripted_triggers/fh_constitutional_dynasties.txt#L61) and the Zhu regency pattern. Keep this separate from the stricter crown check used to finish the journal. Add a completed Zheng settlement check using that live crown, route 3, and `fh_constitution_followup_complete`; share it between the Catholic flag and **Kingdom of Tungning** in [the dynamic names](../common/dynamic_country_names/fh_country_names.txt#L9). Only the flag also requires `country_has_state_religion = rel:catholic`. A Church and State law change alone does not lower the cross if the scripted religion is still Catholic.
4. **Match the writing to the audience.** Use the [storyline](../storyline.md) as the guide for English event text. Show the two names together in the [opening audience or Zheng chronicle](../localization/english/fh_tungning_l_english.yml#L42). Audit the remaining uses of Tungning in English localization, starting with the home army name and the internal proclamation in [the mainland events](../localization/english/fh_mainland_claim_l_english.yml#L23); retain the name in the public interface and in foreign correspondence. Distinguish ratification from the flag change in [the constitutional journal](journals/05-constitutional-settlement.md) and describe the opening banner in [the README](../README.md).

## Static verification

- Trace the `TWG` table for the opening Catholic monarchy, release previews, later changes of faith, reassertion, all renunciation outcomes, tributary status, and the three constitutional paths. Check civic law before the Convention ends, cabinet vacancy, ordinary succession, a Zhu or Zheng regency, suspension and reactivation of the Zhu charter, another house taking the throne, and loss of republican law. Verify that native revolutionary overrides and subject cantons still compose as intended.
- Trace a mainland capital move and the reunification proclamation separately from forming `MIG`. Compare the Ming formation preview and formed flag, then trace full ownership of Beijing and Nanjing separately and together, loss of each seat, and changes to civic, council, and anarchist government. Confirm no new persistent flag state is needed and existing saves resolve from their current law, dynasty, faith, territory, and settlement markers.
- Preview the rectangle and reduced-size canton offline. Run standalone Tiger after scripting to check flag, coat of arms, texture, and localization references, and run `git diff --check`. Follow [AGENTS.md](../AGENTS.md) for validation.

The plan does not add a flag selection decision, a separate naval ensign, changes to claims or religious law, or new flags for `MIG` or foreign powers.
