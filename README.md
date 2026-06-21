
# GVC Reshoring Vulnerability and Post-2020 Trade Balance Shifts

### Part 6 of the *Europe Under Pressure* Series

Does reshoring vulnerability predict trade balance shifts after 2020? A panel regression analysis across EU-27 countries using World Bank WDI data.

---

## Research Question

Did EU countries with higher reshoring vulnerability (from Part 5) experience systematically different trade balance outcomes after 2020?

## Key Finding

**No significant relationship found** (β = 0.0153, p = 0.717).

High-RVI countries did not experience statistically different trade balance shifts post-2020 compared to low-RVI countries, after controlling for country and year fixed effects. This null result is consistent with the recurring pattern across the Europe Under Pressure series.

> Reshoring rhetoric has intensified since 2020 — but the aggregate trade data does not yet show a systematic realignment along GVC vulnerability lines.

## Methodology

**Dependent variable:** Trade balance (% GDP) = Exports − Imports (World Bank WDI, goods & services)

**Key variable:** Reshoring Vulnerability Index (RVI) × Post2020 dummy (interaction term)

**Model:** Two-way Fixed Effects Panel OLS
- Entity fixed effects (country-level)
- Time fixed effects (year-level)
- Clustered standard errors (by country)

**Sample:** EU-27, 2015–2023 (Slovakia dropped due to missing data)

## Results

| Parameter | Value |
|---|---|
| Coefficient (RVI × Post2020) | +0.0153 |
| P-value | 0.717 |
| Observations | 234 |
| Countries | 26 |
| Time periods | 9 (2015–2023) |
| Model | Two-way FE PanelOLS |

## Visualisations

| Figure | Description | Link |
|---|---|---|
| Scatter | RVI vs Trade Balance Change | [View Chart](https://poonum-malhi.github.io/GVC-Reshoring-Trade-Balance-EU/fig_part6_scatter.html) |
| Bar Chart | Pre vs Post 2020 by country | [View Chart](https://poonum-malhi.github.io/GVC-Reshoring-Trade-Balance-EU/fig_part6_bar.html) |
| Change Chart | Trade balance change ranked | [View Chart](https://poonum-malhi.github.io/GVC-Reshoring-Trade-Balance-EU/fig_part6_change.html) |

## Data Sources

- **World Bank WDI** — Exports/Imports of goods & services (% GDP), 2015–2023
- **Part 5 RVI scores** — Constructed from OECD TiVA 2023

## Tools

`Python` `pandas` `numpy` `plotly` `linearmodels` `PanelOLS`

## Limitations

1. Trade balance uses goods & services combined — goods-only series unavailable cleanly from WDI
2. Post-2020 period includes COVID disruption (2020), energy crisis (2022), and gradual normalization — difficult to isolate reshoring signal
3. RVI is a 2020 snapshot — does not capture dynamic GVC repositioning
4. Slovakia excluded due to missing data

## Europe Under Pressure — Full Series

| Project | Question | Key Result |
|---|---|---|
| [Part 1 — China Shock](https://github.com/Poonum-Malhi/china-shock-europe) | Did Chinese imports raise EU unemployment? | p=0.3 — No |
| [Part 2 — AI Shock](https://github.com/Poonum-Malhi/Europe-under-pressure-first-China-now-AI) | Does AI exposure raise EU unemployment? | p=0.518 — No |
| [Part 3 — Climate Shock](https://github.com/Poonum-Malhi/climate-shock-europe) | Does CBAM exposure raise EU unemployment? | p=0.009 — Significant, negative |
| [Part 4 — Housing Shock](https://github.com/Poonum-Malhi/Housing-Affordability-Shock-Index) | Does housing unaffordability raise unemployment? | p=0.66 — No |
| [Part 5 — GVC & Reshoring](https://github.com/Poonum-Malhi/Europe-Global-Value-Chains-Future-shocks) | Which EU countries are most reshoring-exposed? | Czechia, Ireland, Slovakia most vulnerable |
| **Part 6 — Trade Balance** (this repo) | **Does RVI predict post-2020 trade balance shifts?** | **p=0.717 — No significant effect** |

## Root Paper

Antràs, P., & Chor, D. (2013). Organizing the Global Value Chain. *Econometrica*, 81(6), 2127–2204.

---

*Part of the Europe Under Pressure research series, exploring structural economic shocks across the EU.*

