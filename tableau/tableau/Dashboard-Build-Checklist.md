# Tableau Dashboard Build Checklist

1. Connect to `data/nyc_vital_records_enriched.csv`.
2. Set `quarter_start` to Date.
3. Create calculated fields from `Calculated-Fields.txt`.
4. Create global filters: `topic`, `metric`, `submetric`, `year`, `quarter`.
5. Build sheets:
   - KPI latest values: filter to latest quarter + selected metric/submetric.
   - Quarterly line trend: columns `quarter_start`, rows `SUM(value)`, color `submetric`.
   - Cause heatmap: columns `year_quarter`, rows `submetric`, color `SUM(value)`, filter `metric = Deaths by cause`.
   - Birth equity bars: filter `metric` to race/ethnicity, borough, maternal age views.
   - IMR comparisons: filter topic to Infant mortality, line by submetric.
6. Assemble dashboards:
   - Executive Overview
   - Birth Equity & Maternal Health
   - Mortality & Cause Trends
   - Infant Mortality Focus
7. Add a caveat text box: provisional data, lag, overdose six-month lag, infant mortality smoothing, race/ethnicity limitations.
8. Publish as Tableau Public or Tableau Server workbook.
