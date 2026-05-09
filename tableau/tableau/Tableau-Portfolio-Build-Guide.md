# Tableau Portfolio Build Guide — NYC Vital Signs Monitor

Goal: publish a polished public Tableau dashboard under **Karl Appel** that demonstrates data prep, calculated fields, filtering, trend analysis, public-health interpretation, and dashboard design.

## Fastest build option
Use the main data source:

`projects/nyc-vital-records-bi/data/nyc_vital_records_enriched.csv`

This single long-format table is best because it shows you can work with normalized BI data.

## Dashboard title
**NYC Vital Signs Monitor: Provisional Birth & Death Trends**

Subtitle:
Quarterly provisional NYC birth, maternal-health, infant-mortality, and mortality indicators from NYC Department of Health and Mental Hygiene.

Author line:
**Created by Karl Appel**

## Global filters to add
- `topic`
- `metric`
- `submetric`
- `year`
- `quarter`

## Sheet 1 — Births vs Deaths Trend
Purpose: executive trend overview.

Steps:
1. New Sheet → rename `Births vs Deaths Trend`.
2. Drag `quarter_start` to Columns.
3. Drag `value` to Rows.
4. Drag `metric` to Color.
5. Filter `metric` to only:
   - `Total births`
   - `Total deaths`
6. Filter `submetric` to `Total`.
7. Marks type: Line.
8. Turn on labels for line ends if desired.

Portfolio talking point:
“I used a normalized metric/submetric model and filtered to comparable count measures to avoid mixing counts, percentages, and rates.”

## Sheet 2 — Births by Borough — Latest Quarter
Purpose: geographic distribution without needing shape files.

Steps:
1. New Sheet → rename `Latest Births by Borough`.
2. Filter `metric` to `Births by borough`.
3. Filter `quarter_start` to the latest quarter.
4. Exclude `Non-NYC Residents`.
5. Drag `submetric` to Rows.
6. Drag `value` to Columns.
7. Sort descending.
8. Marks type: Bar.
9. Drag `value` to Label.

## Sheet 3 — Maternal Health Indicators
Purpose: show health-system signal over time.

Steps:
1. New Sheet → rename `Maternal Health Indicators`.
2. Filter `metric` to:
   - `Prenatal care in first trimester`
   - `Breastfed infants`
   - `Pre-pregnancy diabetes`
   - `Pre-pregnancy hypertension`
3. Drag `quarter_start` to Columns.
4. Drag `value` to Rows.
5. Drag `metric` to Color.
6. Marks type: Line.
7. Format value axis as Percent.

Design note: diabetes/hypertension are lower percentages than prenatal/breastfeeding, so this works well as small multiples too: drag `metric` to Rows and `quarter_start` to Columns.

## Sheet 4 — Deaths by Cause — Latest Nonblank Quarter
Purpose: public-health mortality profile.

Steps:
1. New Sheet → rename `Latest Deaths by Cause`.
2. Filter `metric` to `Deaths by cause`.
3. Filter `quarter_start` to latest quarter with drug-related deaths available, currently `2025 Q2`, because drug-related deaths lag.
4. Drag `submetric` to Rows.
5. Drag `value` to Columns.
6. Sort descending.
7. Marks type: Bar.
8. Use a contrasting color for `Drug-related` if you want to call out the lag-sensitive category.

## Sheet 5 — Infant Mortality Trend
Purpose: equity and risk signal.

Steps:
1. New Sheet → rename `Infant Mortality Trend`.
2. Filter `metric` to:
   - `Total IMR`
   - `IMR by borough`
3. Drag `quarter_start` to Columns.
4. Drag `value` to Rows.
5. Drag `submetric` to Color.
6. Marks type: Line.
7. Format axis as “per 1,000 live births.”

Caveat: NYC states infant mortality rates are four-quarter moving averages.

## Sheet 6 — Births by Maternal Race/Ethnicity — Latest Quarter
Purpose: demonstrate demographic segmentation.

Steps:
1. New Sheet → rename `Births by Maternal Race/Ethnicity`.
2. Filter `metric` to `Births by maternal race/ethnicity`.
3. Filter `quarter_start` to latest quarter.
4. Drag `submetric` to Columns.
5. Drag `value` to Rows.
6. Marks type: Bar.
7. Sort descending.

## Dashboard layout
Create a new Dashboard named:

`NYC Vital Signs Monitor`

Recommended size:
- Automatic, or 1200 × 900 for desktop portfolio viewing.

Layout:
1. Top title block:
   - NYC Vital Signs Monitor: Provisional Birth & Death Trends
   - Created by Karl Appel
   - Source: NYC DOHMH provisional vital statistics
2. Top row: KPI cards or the `Births vs Deaths Trend` across the width.
3. Middle row:
   - Latest Births by Borough
   - Maternal Health Indicators
4. Bottom row:
   - Latest Deaths by Cause
   - Infant Mortality Trend
5. Footer caveat:
   Data are provisional and subject to change. Most indicators lag approximately three months; drug-related deaths lag approximately six months. Infant mortality rates are four-quarter moving averages.

## Public publishing
1. File → Save to Tableau Public As...
2. Sign in to Karl Appel’s Tableau Public account.
3. Workbook name:
   `NYC Vital Signs Monitor - Provisional Birth and Death Trends`
4. Copy the public URL after publish.

## Suggested portfolio blurb
Built an interactive Tableau dashboard using NYC Department of Health provisional vital-statistics data. The dashboard uses a normalized long-format dataset, calculated quarter fields, metric filters, public-health caveats, and multiple visual encodings to compare birth trends, maternal-health indicators, infant mortality, and mortality causes over time.
