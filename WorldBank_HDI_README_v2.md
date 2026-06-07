# 🌍 World Bank & UN HDI — Global Development Analysis (v2)
**by Oluwafemi Adesanya (Femi)** · Data Analyst | Prompt Engineer

---

## Project Overview

As part of an **International Development Association (IDA)** analyst team simulation, this project delivers a comprehensive data-driven presentation for IDA leadership, answering four critical development questions using real World Bank and UN Human Development Index (HDI) data.

> **Datasets span 1990–2021 across 190+ countries, 7 regions, and 4 income groups.**

---

## Datasets Used

| Dataset | Source | Coverage |
|---|---|---|
| `WorldBank.xlsx` | World Bank Open Data | 1960–2018 · 12,449 records · 15 indicators |
| `HDI.csv` | UN Human Development Reports | 1990–2021 · 206 countries · 1,008 columns |
| `world_indicators_data_dictionary.csv` | World Bank | Field definitions for all indicators |

### Key Indicators Analysed
- GDP (USD) & GDP per capita
- Life expectancy at birth
- Infant mortality rate
- Electric power consumption
- Internet usage
- Birth & death rates
- Human Development Index (HDI)
- Income group classifications

---

## Business Questions Answered (In Priority Order)

### 1. Population & GDP Growth from 1990 — Is There Overlap?

**Top 10 GDP growth countries (1990 onwards):**

| Country | GDP Growth | Region |
|---|---|---|
| Equatorial Guinea ★ | +11,778% | Sub-Saharan Africa |
| Vietnam | +3,686% | East Asia & Pacific |
| China | +3,667% | East Asia & Pacific |
| Qatar ★ | +2,509% | Middle East & North Africa |
| Maldives | +2,351% | South Asia |

**Top 10 population growth countries (1990 onwards):**

| Country | Pop Growth | Region |
|---|---|---|
| Qatar ★ | +484% | Middle East & North Africa |
| UAE | +427% | Middle East & North Africa |
| Equatorial Guinea ★ | +212% | Sub-Saharan Africa |
| Afghanistan | +200% | South Asia |
| Bahrain | +181% | Middle East & North Africa |

**Overlap:** Qatar and Equatorial Guinea appear in **both** top 10 lists — the only two countries with explosive growth in both GDP and population since 1990.

> China grew from **$0.36 trillion in 1990 to $13.6 trillion in 2018** — the largest absolute GDP expansion of any nation in the dataset.

---

### 2. Which Regions Grew HDI Most in the 21st Century?

| Region | HDI 2000 | HDI 2021 | Growth |
|---|---|---|---|
| Sub-Saharan Africa | 0.437 | 0.544 | **+24.5%** |
| South Asia | 0.528 | 0.654 | **+24.0%** |
| East Asia & Pacific | 0.607 | 0.691 | +13.8% |
| Arab States | 0.640 | 0.718 | +12.2% |
| Europe & Central Asia | 0.659 | 0.772 | +17.1% |
| Latin America | 0.670 | 0.740 | +10.4% |

> **COVID-19 impact:** All regions recorded an HDI dip in 2020 — demonstrating how fragile development gains are without structural investment.

---

### 3. Which Factors Are Most Correlated with Life Expectancy?

| Factor | Correlation | Direction |
|---|---|---|
| Infant mortality | **–0.939** | Negative — strongest predictor |
| Birth rate | –0.877 | Negative |
| Death rate | –0.841 | Negative |
| Internet access | +0.598 | Positive |
| Electricity consumption | +0.539 | Positive |
| GDP per capita | +0.522 | Positive |
| Unemployment | +0.010 | Almost no effect |

> Internet access (0.598) predicts life expectancy **more strongly than GDP per capita (0.522)** — infrastructure investment delivers outsized development returns.

---

### 4. What Differentiates High Income vs Low Income Countries?

| Indicator | Low Income | Lower Middle | Upper Middle |
|---|---|---|---|
| Life expectancy | 49 years | 59 years | 66 years |
| Infant mortality | 106 per 1,000 | 69 per 1,000 | 41 per 1,000 |
| GDP per capita | $355 | $1,040 | $3,210 |
| Internet access | 3% | 11% | 19% |

> Low income countries have a **6× internet access gap** vs upper-middle income nations (3% vs 19%) — the single most actionable infrastructure target.

---

## 3 Insights for the Next IDA Budget Cycle

| # | Insight | Data Point | Recommended Action |
|---|---|---|---|
| 1 | Infant mortality is the single biggest threat to life expectancy — and it's preventable | Correlation = **–0.939**, highest of any factor | Fund maternal & infant health programmes |
| 2 | SSA is making real progress but gains are fragile | SSA HDI rose from **0.437 → 0.543** (2000–2021), +24.5% — highest globally | Increase and sustain IDA allocation to SSA |
| 3 | Internet access delivers more impact than GDP investment alone | **6× internet gap** between low and upper-middle income countries (3% vs 19%) | Invest in digital infrastructure in low income nations |

---

## Prompt Engineering — Score Progression

This project demonstrates iterative prompt improvement across two versions:

### Version 1 — Score: 9.0/10
```
As part of the International Development Association (IDA) analyst team, you have been 
tasked to provide a comprehensive presentation for IDA leaders, the following questions 
in that order of priority using the uploaded data set.
- Which countries have experienced the highest growth in population and GDP? Is there overlap?
- Where regions saw the most growth in HDI in the 21st century?
- Which factors are highly correlated with life expectancy?
- Which factors differentiate 'High Income' vs 'Low Income' Countries?
Provide KPIs, with interactive dark-themed dashboards using varying graphs. Keep it simple 
— no jargon. Initial overview or summary at the beginning. Flag exactly 3 insights IDA 
leaders would need to act on immediately.
```

### Version 2 — Score: 9.5/10
```
As part of the International Development Association (IDA) analyst team, you have been 
tasked to provide a comprehensive presentation for IDA leaders, the following questions 
in that order of priority using the uploaded data set.
- Which countries have experienced the highest growth in population and GDP from 1990 
  onwards? Is there overlap?
- Where regions saw the most growth in HDI in the 21st century?
- Which factors are highly correlated with life expectancy?
- Which factors differentiate 'High Income' vs 'Low Income' Countries?
Provide KPIs, with interactive dark-themed dashboards using varying graphs - scattered 
to lines and charts as deemed fit. Keep it simple — no jargon. Initial overview or 
summary at the beginning.
Flag exactly 3 insights IDA leaders would act on in their next budget cycle. Support 
each with one specific data point from the dataset.
```

### What changed — and why it mattered

| Change | Impact |
|---|---|
| Added "from 1990 onwards" | Removed historical outliers — results reflect the modern development era |
| "Next budget cycle" | Framed insights as decisions, not observations |
| "Support with one specific data point" | Every insight is now pinned to evidence — boardroom-ready |

**New finding unlocked by the 1990 filter:** Qatar and Equatorial Guinea are the only two countries in **both** top 10 lists — a genuinely important overlap obscured in the unfiltered data.

---

## Prompt Score Summary

| Version | Score | Key improvement |
|---|---|---|
| v1 | 9.0 / 10 | Strong structure, clear questions, dark theme |
| v2 | 9.5 / 10 | Time boundary added, data-backed insights, budget framing |

---

## Output Files

| File | Description |
|---|---|
| `IDA_dashboard_v2.html` | Interactive dark-themed dashboard (v2) |
| `WorldBank.xlsx` | World Bank dataset (1960–2018) |
| `HDI.csv` | UN HDI dataset (1990–2021) |
| `world_indicators_data_dictionary.csv` | Field definitions |
| `WorldBank_HDI_README.md` | This file |

---

## Skills Demonstrated

- Multi-dataset analysis (3 files joined and cross-referenced)
- Correlation analysis across 7 indicators
- Regional & income group comparisons
- Long-range trend analysis (1990–2021)
- Iterative prompt engineering with scored improvement
- Dashboard design for executive/leadership audiences
- Evidence-backed insight framing

---

## Part of My Prompt Engineering Portfolio

👉 [github.com/iamabeke/prompt-engineering-portfolio](https://github.com/iamabeke/prompt-engineering-portfolio)

---

*Project completed June 2026 · Tools: Claude (Anthropic) · Data: World Bank & UN HDI*
