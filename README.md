# Executive Sales KPI Dashboard

**Status:** 🚧 In progress

## Business question
How is the business performing against targets, and where should leadership focus?

## Data
- **Source:** [e.g. Superstore Sales or Contoso/AdventureWorks sample]
- **Model:** [star schema: 1 fact table + date, product, customer, region dimensions]

## Tools
Power BI · DAX · Power Query

## Approach
1. Cleaned and shaped data in Power Query
2. Built a star-schema data model with a proper date table
3. Wrote DAX measures (see below)
4. Designed a one-page layout: KPI cards on top, trends in the middle, breakdowns below, with slicers for date, region, and category

## Key DAX measures
```dax
Total Sales = SUM(Sales[Revenue])
Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))
YoY Growth % = DIVIDE([Total Sales] - [Sales LY], [Sales LY])
Profit Margin % = DIVIDE(SUM(Sales[Profit]), [Total Sales])
```

## Key insights
- [Insight 1 with a number]
- [Insight 2]
- [Insight 3]

## Preview
![Dashboard screenshot](dashboard/screenshot.png)

🎥 [1-2 minute walkthrough video](link)

## Files
- [`dashboard/sales-report.pbix`](./dashboard/sales-report.pbix) (open in Power BI Desktop)
- `dashboard/screenshot.png`

## Repo structure
```
data/        dataset or download link
dashboard/   .pbix file, screenshots
```
