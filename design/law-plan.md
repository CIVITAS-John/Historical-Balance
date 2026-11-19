# Qing, Tungning, and Sinosphere law plan

## Laws against vanilla

The right column lists what changes. Other law effects and restrictions carry over.

| Baseline | Mod changes |
| --- | --- |
| **Appointed Bureaucrats:** +50% bureaucrat political strength, +25% tax capacity. | **Standardized Examinations:** −5% population bureaucracy cost and −5% technology spread. Education access: −3 points plus 0.3 per wealth level. Requires a Sinosphere primary culture. Đại Nam, Qing, and Tungning start with it. |
| **Hereditary Bureaucrats:** −25% population bureaucracy cost, +25% aristocrat political strength. Joseon starts on Appointed Bureaucrats under a regency. | **Yangban Administration:** −30% population bureaucracy cost, +35% aristocrat political strength. Joseon only; replaces its starting law. |
| **Serfdom:** +25% Landowner political strength, 75% minimum subsistence land share, 50% minimum subsistence employment modifier, peasant migration and economic law restrictions. | **Banner Estates:** Qing starts with +30% Landowner political strength and a 65% minimum subsistence land share. |
| **Subjecthood:** +100 authority, 100 base primary culture acceptance, 30 homeland acceptance, −25% assimilation. | **Mandate of Heaven:** Reduce decree cost by 10%. Set assimilation to −35%. Requires Monarchy. Qing starts with it. Southern Ming adopts it if Port and Village Registers are still active; otherwise restoration unlocks it. |
| **Unamended Mandate of Heaven:** No Manchu preference or conscription modifier. | **Banner Precedence:** Qing starts with **+1 living standard for Manchu Pops, −0.5 for all others**, −10 non-Manchu acceptance, and −50% conscription rate. Living standard changes create 25% more radicals on declines and 25% more loyalists on gains. Permanently removed when the Taiping Rebellion diplomatic play starts against Qing. |
| **Subjecthood:** +100 authority and 30 homeland acceptance. | **Port and Village Registers:** Tungning starts with this amendment, sponsored by the Army and Fleet. It raises homeland acceptance to 40, including for Indigenous Pops in their homelands, and adds +25% conscription until [the first mainland registration](journals/06-mainland-reconquest.md#consolidate-the-foothold). |
| **Canton System:** Canton is the only licensed gateway. +50 Trade Center limit, −25% trade capacity, +25% authority, +15% tax capacity, +75% leverage resistance, −10% technology spread. | **Coastal Registers:** Qing’s Industrialists sponsor this starting amendment. It sets trade capacity to −20%, technology spread to −5%, and authority to +10%. It uses Free Trade for political stances and can only attach to the Canton System. Permanently removed when Qing directly owns all Taiwan, even if Tungning survives elsewhere. |
| **Mercantilism:** +25% export and −25% import advantage; export/import tariff allowances 20%/50%, subsidy allowances 50%/20%. | **Anping Trade Charters:** Tungning starts with +35% export advantage and a 10% export tariff allowance. |
| **Religious Schools:** Per level, +10 points of education access, +20% conversion speed, +10% Devout political strength. −20% institution cost. Requires Rationalism; incompatible with Total Separation, State Atheism, and Serfdom. | **Confucian Academies:** Per level, +8 points of education access plus 0.4 points per wealth level. −40% educational institution cost; no conversion bonus. Requires an official Confucian faith and allows Banner Estates. Joseon starts at level 1 and can keep Serfdom alongside the Academies. |
| **Religious Schools:** +20% conversion speed per level. | **Tungning School Charter:** Tungning starts with level 1 Religious Schools and this amendment, sponsored by the School of Practical Learning. The charter cancels the conversion bonus at every level. |
| **Freedom of Conscience:** +100 authority, +15% Devout political strength. Official/nonofficial wages +5%/−5%. Religious acceptance +20/+15/+5/0 for official faith, shared trait, shared trait group, or no match. | **Yongli Articles of Conscience:** Tungning starts with this amendment: +10 religious acceptance for a shared trait group, +5 for no match, and −50% conversion speed. |

Tungning keeps Min, Han, and Hakka as primary cultures; the Registers have no religious condition. Tungning starts with Professional Army.

If an active academy law loses its required faith, use the first legal fallback: Religious Schools, Private Schools, then Public Schools if compulsory education or a power bloc rule bars No Schools; otherwise No Schools. Preserve investment while schools remain active. If no fallback is legal, keep the Academies and check again after laws change and on the monthly pulse.

## Implementation and checks

- **Banner subsidies:** Use `state_standard_of_living_add = -0.5` plus `state_manchu_standard_of_living_add = 1.5`. The living standard gap can already fuel secession. Use `country_expenses_add` if the subsidy should also cost the treasury.
- **Amendments:** Apply only on matching laws. Use direct ownership with a monthly fallback for Taiwan and the exact diplomatic play start for Taiping. Record permanent removals even if the underlying law has changed.
- **Court faith:** Follow the [settlement design](journals/02-court-faith.md#settlement). Use a narrow Church and State group override for the enactment lock and guard repeal separately. Mods overriding the same group need a compatibility patch. [Ming restoration](journals/05-constitutional-settlement.md#the-southern-court-reborn--ming-restoration) keeps the country tag and any citizenship law the player enacted.
- **Subjecthood compatibility:** The Registers use vanilla Subjecthood directly. Mandate of Heaven also uses the vanilla Subjecthood discrimination calculation for cultural minority movements. The exact checks in Iberian events, regional character ideologies, and Russian scripts remain scoped to their original laws and content. Vanilla regime transitions that exclude Subjecthood as a replacement citizenship law also exclude the Mandate.
- **Restoration hook:** Call `fh_restore_southern_ming_citizenship = yes` at the Zhu enthronement in Tungning scope. The constitutional restoration journal is still a design; the hook changes only the citizenship law when the Registers remain active and otherwise unlocks the Mandate.

## 1836 setup changes

See the [mod overview](../README.md) for Taiwan’s industry and treaty terms. The Huế Supply Accord binds for five years when the markets can trade; its frigates are separate from Tungning’s fleet. Both Manila Compact branches ship porcelain to Spain; the independent Manila deal is separate.
