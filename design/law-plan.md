# Qing, Tungning, and Sinosphere law plan

## Proposed laws against vanilla

The right column lists only what changes; other effects and restrictions carry over. Joseon and Đại Nam’s bureaucracy starts are in the mod; the other law changes are proposals.

| Baseline | Mod changes |
| --- | --- |
| **Appointed Bureaucrats:** +50% bureaucrat political strength, +25% tax capacity. | **Standardized Examinations:** −5% population bureaucracy cost and −5% technology spread. Education access: −3 points plus 0.25 per wealth level. Requires a Sinosphere primary culture. Đại Nam starts with it; proposed for Qing and Tungning too. |
| **Hereditary Bureaucrats:** −25% population bureaucracy cost, +25% aristocrat political strength. Joseon starts on Appointed Bureaucrats under a regency. | **Yangban Administration:** −30% population bureaucracy cost, +35% aristocrat political strength. Joseon only; replaces its starting law. |
| **Serfdom:** +25% Landowner political strength, 75% minimum subsistence land share, 50% minimum subsistence employment modifier, peasant migration and economic law restrictions. | **Banner Estates:** Qing starts with +30% Landowner political strength and a 65% minimum subsistence land share. |
| **Subjecthood:** +100 authority, 100 base primary culture acceptance, 30 homeland acceptance, −25% assimilation. | **Mandate of Heaven:** Reduce decree cost by 10%. Set assimilation to −35%. Requires Monarchy. Qing starts with it. Southern Ming adopts it if Port and Village Registers are still active; otherwise restoration unlocks it. |
| **Unamended Mandate of Heaven:** No Manchu preference, living standard modifier, or officer bonus. | **Banner Precedence:** Qing starts with **+1 living standard for Manchu pops, −0.5 for all others**, -10 non-Manchu acceptance, and +25% radicals from living standard decrease. Permanently removed when the Taiping Rebellion diplomatic play starts against Qing. |
| **Subjecthood:** +100 authority and 30 homeland acceptance. | **Port and Village Registers:** Tungning starts with 40 homeland acceptance, including for Indigenous pops in their homelands. |
| **Canton System:** Canton is the only licensed gateway. +50 Trade Center limit, −25% trade capacity, +25% authority, +15% tax capacity, +75% leverage resistance, −10% technology spread. | **Coastal Registers:** Qing starts with this amendment: Set to −20% trade capacity, -5% technology spread, but only +10% authority. Permanently removed when Qing directly owns all Taiwan, even if Tungning survives elsewhere. |
| **Mercantilism:** +25% export and −25% import advantage; export/import tariff allowances 20%/50%, subsidy allowances 50%/20%. | **Anping Trade Charters:** Tungning starts with +35% export advantage and a 10% export tariff allowance. |
| **Religious Schools:** Per level, +10 points of education access, +20% conversion speed, +10% Devout political strength. −20% institution cost. Requires Rationalism; incompatible with Total Separation, State Atheism, and Serfdom. | **Confucian Academies:** Per level, +8 points of education access, <!--a bit of wealth access to balance out at 12-->, -40% educational institution cost; remove the conversion bonus. Requires an official Confucian faith; allows Banner Estates. |
| **Freedom of Conscience:** +100 authority, +15% Devout political strength. Official/nonofficial wages +5%/−5%. Religious acceptance +20/+15/+5/0 for official faith, shared trait, shared trait group, or no match. | **Yongli Articles of Conscience:** Tungning starts with this amendment: +10 religious acceptance for a shared trait group, +5 for no match, and -50% conversion<!-- reducing the JE conversion debuff-->. |

Tungning keeps Min, Han, and Hakka as primary cultures; the Registers have no religious condition. No country starts with Confucian Academies.

If an active academy law loses its required faith, use the first legal fallback: Religious Schools, Private Schools, then Public Schools if compulsory education bars No Schools; otherwise No Schools. Preserve investment while schools remain active.

## Implementation and checks

- **Banner subsidies:** Use `state_standard_of_living_add = -0.5` plus `state_manchu_standard_of_living_add = 1.5`. The living standard gap can already fuel secession. Use `country_expenses_add` if the subsidy should also cost the treasury.
- **Amendments:** Apply only on matching laws. Use direct ownership with a monthly fallback for Taiwan and the exact diplomatic play start for Taiping. Record permanent removals even if the underlying law has changed.
- **Court faith:** Follow the [settlement design](journals/02-court-faith.md#settlement). Use a narrow Church and State group override for the enactment lock and guard repeal separately. Mods overriding the same group need a compatibility patch. [Ming restoration](journals/05-constitutional-settlement.md#the-southern-court-reborn--ming-restoration) keeps the country tag and any citizenship law the player enacted.
- **Static checks:** Verify vanilla rules that check for Subjecthood exactly. Trace mixed cultures, partial and full Taiwan ownership, the Taiping trigger, court settlement, and cases where no school fallback is legal.

## 1836 setup changes

See the [mod overview](../README.md) for Taiwan’s industry and treaty terms. The Huế Supply Accord binds for five years when the markets can trade; its frigates are separate from Tungning’s fleet. Both Manila Compact branches ship porcelain to Spain; the independent Manila deal is separate.
