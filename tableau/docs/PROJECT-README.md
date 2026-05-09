# NYC Provisional Vital Statistics BI Starter Pack

Source: https://github.com/nychealth/provisional-vital-statistics

This folder turns NYC DOHMH's provisional birth and death CSV into a practical Power BI/Tableau dashboard plan.

## Data used
- File: `data/nyc_vital_records_enriched.csv`
- Source: repo `data_archive.csv`
- Coverage: Jan 2022 through Jul 2025, quarterly
- Rows: 1095
- Metrics: 21
- Nulls: one expected blank for latest drug-related deaths because overdose/drug-death reporting has a longer lag.

## Recommended dashboard: NYC Vital Signs Monitor

Audience: public-health leadership, analysts, policy staff, journalists, grant writers, and civic-health stakeholders.

Core question: **Where are NYC birth, maternal-health, infant-mortality, and mortality indicators improving or worsening by quarter and population group?**

### Page 1 — Executive Overview
KPI cards:
- Latest total births
- Latest total deaths
- Latest infant mortality rate
- Latest prenatal care in first trimester
- Latest cesarean percentage
- Latest drug-related deaths using latest non-null quarter

Visuals:
- Births vs deaths quarterly line chart
- Small multiples for prenatal care, Medicaid coverage, cesarean rate, breastfeeding, pre-term births
- Latest-quarter Top 5 causes of death bar chart
- Annotation/caveat card: provisional data and reporting lag

### Page 2 — Birth Equity & Maternal Health
Filters: quarter/year, race/ethnicity, borough where available, maternal age.

Visuals:
- Births by maternal race/ethnicity trend
- Births by borough trend
- Prenatal care / breastfeeding / Medicaid coverage / pre-pregnancy diabetes / hypertension KPI trends
- Birth outcome rates: pre-term, very pre-term, low birthweight, very low birthweight

### Page 3 — Mortality & Cause Trends
Filters: quarter/year, age group, sex, race/ethnicity, cause.

Visuals:
- Total deaths trend
- Deaths by age stacked bar over time
- Deaths by cause heatmap: cause x quarter
- Drug-related deaths trend with six-month lag caveat
- Race/ethnicity and sex breakdown comparison

### Page 4 — Infant Mortality Focus
Filters: quarter/year, borough, race/ethnicity, neonatal/post-neonatal.

Visuals:
- Total IMR line chart
- IMR by borough/race grouped bars
- Neonatal vs post-neonatal trend
- Note: infant mortality rates are four-quarter moving averages per NYC documentation.

## Caveats to display in the dashboard
- Data are provisional and subject to change, especially recent quarters.
- Most indicators lag about three months.
- Overdose/drug-related death data lag about six months.
- Infant mortality rates are smoothed using four-quarter moving averages.
- Race/ethnicity categories include an “Other/Unknown” group; some populations are underrepresented due to confidentiality/reporting limitations.

## Files
- `data/nyc_vital_records_enriched.csv` — BI-ready long table with quarter/year/topic fields added
- `data/metrics_dictionary.json` — metric/submetric inventory
- `powerbi/PowerQuery-M.txt` — direct Power BI query from GitHub raw CSV
- `powerbi/DAX-Measures.txt` — starter measures
- `tableau/Calculated-Fields.txt` — starter calculated fields
- `tableau/Dashboard-Build-Checklist.md` — Tableau build steps
