# Tableau Final Handoff — NYC Vital Signs Monitor

## Working local workbook

Use this file:

`projects/nyc-vital-records-bi/tableau/nyc_vital_records_monitor_portfolio_final.twbx`

Verified on May 8, 2026: it opens in Tableau Public with no error dialog.

Visible tabs:
- `Data Source`
- `Births vs Deaths Trend`
- `Births vs Deaths Summary`
- `NYC Vital Signs Monitor`

Dashboard contents:
- Births vs Deaths Trend line chart
- Births vs Deaths Summary bar chart

## Source data / starter data

Main BI-ready source:

`projects/nyc-vital-records-bi/data/nyc_vital_records_enriched.csv`

Prepared Tableau chart extracts:

`projects/nyc-vital-records-bi/tableau/portfolio-data/`

Files:
- `00_kpi_cards.csv`
- `01_births_vs_deaths_trend.csv`
- `02_latest_births_by_borough.csv`
- `03_maternal_health_indicators.csv`
- `04_latest_deaths_by_cause.csv`
- `05_infant_mortality_trends.csv`
- `06_latest_births_by_maternal_race_ethnicity.csv`

## Build guide

Detailed manual expansion guide:

`projects/nyc-vital-records-bi/tableau/Tableau-Portfolio-Build-Guide.md`

Recommended remaining sheets to add manually in Tableau:
1. Latest Births by Borough
2. Maternal Health Indicators
3. Latest Deaths by Cause
4. Infant Mortality Trend
5. Births by Maternal Race/Ethnicity

## Notes

- Direct Tableau UI automation is partially working after Accessibility access was enabled.
- Drag/drop dashboard automation is unreliable, but menu access and saving/exporting work.
- A generated six-sheet TWB candidate was tested and rejected because Tableau refused to load it with XML/layout schema errors. Do not use `nyc_vital_records_monitor_6sheet_candidate.twb`.
- The working `.twbx` is the safe artifact to publish or continue editing.

## Publish step

Publishing to Tableau Public is an external/public action. Do not publish without explicit CEO approval.
