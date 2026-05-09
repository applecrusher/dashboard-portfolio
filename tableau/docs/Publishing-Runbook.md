# Publishing Runbook: Tableau Public + Power BI Public Link

## Tableau Public
1. Open Tableau Public Desktop.
2. Connect to `data/nyc_vital_records_enriched.csv`.
3. Build the four dashboard tabs from `tableau/Dashboard-Build-Checklist.md`.
4. Add the title/caveat/source text from `publish/Public-Dashboard-Copy.md`.
5. Save to Tableau Public.
6. Copy the Tableau Public dashboard URL.

Public link format usually looks like:
`https://public.tableau.com/views/<workbook>/<dashboard>`

## Power BI
Power BI public sharing requires Power BI Service and tenant permission for “Publish to web.”

1. Open Power BI Desktop.
2. Get Data → Web or Blank Query → paste the M query from `powerbi/PowerQuery-M.txt`.
3. Rename table to `VitalStats`.
4. Add DAX measures from `powerbi/DAX-Measures.txt`.
5. Build the same four pages.
6. Publish to Power BI Service workspace.
7. In Power BI Service: File → Embed report → Publish to web (public).
8. Copy the public link or iframe embed URL.

Public link format usually looks like:
`https://app.powerbi.com/view?r=<token>`

## Safety check before sharing
- No private data is included. This source is public NYC DOHMH open data.
- Caveat/attribution must be visible on both dashboards.
- Drug-related death KPI should use latest nonblank quarter, not the blank latest row.
