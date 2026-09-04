# Travel Pulse — Updated Excel Dashboard

## What's updated
- Dashboard data is rebuilt from `18August2026_Travel Pulse_Escalent_Dataset(2).xlsx`.
- Uses all 1,418 completed respondents in the workbook.
- Existing Travel Pulse layout, tabs, filter UI and login flow are retained.
- All dashboard filters can be combined; changing one filter no longer discards the others.
- Bar charts show the full available category set instead of only the previous top-N display.
- Long charts automatically grow vertically so categories remain readable and scroll naturally with the page.
- Pie/donut slices and legends are clickable and act as dashboard filters.
- Bars, decision-list items and other categorical chart elements are also clickable filters.
- Reset clears both dropdown filters and chart-click filters.
- Filter menus remain scrollable for large option sets such as household income.
- Chart PNG export remains available.
- Survey base is populated dynamically from the new dataset.

## Run
From this folder:

```bash
python -m http.server 8000
```

Open:

`http://localhost:8000/`

## Login
Default credentials remain:

- Username: `admin`
- Password: `TravelPulse2026`

## Important
This is client-side authentication suitable for a local/internal static demo. The credentials are visible in browser source and are not server-side security.


## Full survey coverage
- Added an **All Survey Questions** tab covering Q2–Q24 where the source workbook contains the question.
- Q13 is explicitly marked as absent because it is not present in the supplied Excel workbook.
- Q3/Q3a text responses are shown as ranked distributions.
- Q8a booking order is shown as first-booked share plus average rank.
- Q18 is shown as a scrollable airline strategy × carrier matrix (all source matrix cells).
- Q24 is shown as a scrollable hotel strategy × brand matrix (all source matrix cells).
- Long bar charts use an internal vertical scrollbar rather than overflowing their cards.
- Fixed the carrier chart axis so bars can never exceed the plotting area when the configured axis ceiling is below the actual data maximum.
