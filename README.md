# NYC Tableau Vital Records Package

This folder contains the local Tableau files and data for the NYC Vital Signs Monitor / NYC provisional vital records dashboard work.

## Start here
- Safe working packaged workbook: `tableau/nyc_vital_records_monitor_portfolio_final.twbx`
- Handoff note: `tableau/FINAL-HANDOFF.md`
- Tableau build guide: `tableau/Tableau-Portfolio-Build-Guide.md`
- Dashboard checklist: `tableau/Dashboard-Build-Checklist.md`
- Tableau-ready extract CSVs: `tableau/portfolio-data/`
- Main enriched data: `data/nyc_vital_records_enriched.csv`
- Metric dictionary: `data/metrics_dictionary.json`

## Important file note
The safe local Tableau artifact is:

`tableau/nyc_vital_records_monitor_portfolio_final.twbx`

A generated six-sheet candidate exists in the Tableau folder, but it previously had Tableau XML/layout schema load errors and should not be treated as the safe artifact unless rebuilt/verified manually.

## Public data source links
- NYC DOHMH provisional vital statistics GitHub repo: https://github.com/nychealth/provisional-vital-statistics
- Raw source CSV used upstream: https://raw.githubusercontent.com/nychealth/provisional-vital-statistics/main/data_archive.csv
- NYC Open Data portal: https://opendata.cityofnewyork.us/
- Tableau Public homepage/search: https://public.tableau.com/

## Tableau Public status
No Tableau Public publish URL has been created yet from this workbook. Publishing to Tableau Public is an external/public action and should be done only after explicit approval and a final polish/review pass.

When ready to publish:
1. Open `tableau/nyc_vital_records_monitor_portfolio_final.twbx` in Tableau Public/Desktop.
2. Review dashboard tabs and caveat text.
3. File → Save to Tableau Public As...
4. Use the title: `NYC Vital Signs Monitor - Provisional Birth and Death Trends`.
5. Copy the resulting Tableau Public URL into this README.

## Caveats to show publicly
- Data are provisional and subject to change.
- Most indicators lag approximately three months.
- Drug-related death data lag approximately six months.
- Infant mortality rates are four-quarter moving averages.
- Race/ethnicity categories include Other/Unknown; interpret demographic breakouts carefully.
