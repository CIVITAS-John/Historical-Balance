# Qing, Tungning, and Sinosphere law plan

## Proposed laws against vanilla

Only changes from the named counterpart are listed. Joseon and Đại Nam’s bureaucracy starts are in the mod; the other law changes are proposals.

| Law (counterpart) | Change |
| --- | --- |
| **Standardized Examinations** (Appointed Bureaucrats) | −5% population bureaucracy cost and technology spread; −3 points of education access plus 0.25 per wealth level (breaks even at wealth 12). Available with a Sinosphere primary culture, including Joseon’s. Đại Nam starts with it; Qing and Tungning would also start with it. |
| **Yangban Administration** (Hereditary Bureaucrats) | Set population bureaucracy cost to −30% and aristocrat political strength to +35%. Joseon only; replaces Appointed Bureaucrats at the start and keeps the regency. |
| **Banner Estates** (Serfdom) | Qing starts with +30% Landowner political strength and a 65% minimum subsistence share of incorporated arable land. |
| **Mandate of Heaven** (Subjecthood) | +5 base legitimacy; set base primary culture acceptance to 90 and assimilation to −35%. Requires Monarchy. Qing starts with it. The Southern Ming adopts it only if Port and Village Registers are still active; otherwise restoration unlocks it. |
| **Banner Precedence** (Mandate of Heaven amendment) | Qing starts with **+1 living standard for Manchu pops, −0.5 for all others**, +10 Manchu acceptance, and +10% political strength for all officers. Permanently remove the amendment when the Taiping Rebellion diplomatic play starts against Qing. |
| **Port and Village Registers** (Subjecthood) | Tungning starts with +75 authority and 40 homeland acceptance, including for Indigenous pops in their own homelands. Keeps Min, Han, and Hakka as primary cultures with no religious condition. |
| **Coastal Registers** (Canton System amendment) | Qing starts with a +60 Trade Center limit bonus and −20% trade capacity. Permanently remove it when Qing directly owns all of Taiwan, even if Tungning survives elsewhere. Occupation and tribute don’t count. |
| **Anping Trade Charters** (Mercantilism) | Tungning starts with +35% export advantage and a 10% export tariff allowance. |
| **Confucian Academies** (Religious Schools) | Per level: +8 points of education access, +5% qualifications, +5% Devout political strength, and no conversion bonus. Requires an official Confucian faith; Banner Estates is the only Serfdom exception. No opening school changes. |
| **Yongli Articles of Conscience** (Freedom of Conscience amendment) | Tungning starts with +10 religious acceptance for a shared trait group, +5 for no match, and a −2% wage penalty for nonofficial faiths. |

If an active academy law loses its required faith, use the first legal fallback: Religious Schools, Private Schools, then Public Schools if compulsory education bars No Schools; otherwise No Schools. Preserve investment while schools remain active.

## Implementation and checks

- **Banner subsidies:** Use `state_standard_of_living_add = -0.5` plus `state_manchu_standard_of_living_add = 1.5`. The living standard gap can already fuel secession. Use `country_expenses_add` if the subsidy should also cost the treasury.
- **Amendments:** Apply only on matching laws. Use direct ownership with a monthly fallback for Taiwan and the exact diplomatic play start for Taiping. Record permanent removals even if the underlying law has changed.
- **Court faith:** Follow the [settlement design](journals/02-court-faith.md#settlement). Use a narrow Church and State group override for the enactment lock and guard repeal separately. Mods overriding the same group need a compatibility patch. [Ming restoration](journals/05-constitutional-settlement.md#the-southern-court-reborn--ming-restoration) keeps the country tag and any citizenship law the player enacted.
- **Static checks:** Verify vanilla rules that check for Subjecthood exactly. Trace mixed cultures, partial and full Taiwan ownership, the Taiping trigger, court settlement, and cases where no school fallback is legal.

## 1836 setup changes

See the [mod overview](../README.md) for Taiwan’s industry and treaty terms. The Huế Supply Accord binds for five years when the markets can trade; its frigates are separate from Tungning’s fleet. Both Manila Compact branches ship porcelain to Spain; the independent Manila deal is separate.
