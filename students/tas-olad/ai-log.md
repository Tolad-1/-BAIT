# AI Log — Minnesota Corn Sourcing Signal

## Prompt 1 — project direction
I shared the Harvest to Screen assignment, the BAIT team context, and the existing team GitHub work. I asked for help choosing a decision question and a realistic public agricultural data source.

## Prompt 2 — build the page
Build a self-contained HTML dashboard for a Minnesota food and beverage supply-chain decision. Use the team's existing USDA NASS Minnesota corn-for-grain production data for 2015–2025. Include a year dropdown, metrics, a chart, a data table, source information, limitations, and comments explaining where data comes in, where it is stored, and where it is transformed. The page must load a local CSV copy rather than depend on a live API.

## Prompt 3 — prepare the local dataset and documentation
Normalize the shared USDA CSV into a local `corn-production.csv` with numeric production values and write a README explaining the decision question, source, fields, how to run the page, and limitations.

## One issue caught and how it was checked
The shared CSV represented production values with commas inside quoted numbers (for example, `1,428,800,000`). A simple comma-splitting script would incorrectly split those values into multiple columns or leave them unusable as numbers. I checked the raw CSV rows and normalized the production column into plain numeric values (for example, `1428800000`) in my saved copy. I also checked the annual values against the shared file's 2015–2025 rows.

## Verification notes
- The source is identified as USDA NASS Quick Stats in the team's README and the linked Quick Stats query.
- The shared project CSV has 11 annual rows, 2015–2025.
- The page uses the local `corn-production.csv`; it does not call the USDA website when it runs.
- The original USDA extraction/download date was not recorded in the shared CSV. The copy used for this assignment was downloaded from the team's repository on November 19, 2026; I have stated that distinction rather than claiming the original USDA extraction date is known.
- The chart and percentages are calculations from the stored CSV, not additional USDA observations.

## Final checks to perform
1. Open the page using a local server or GitHub Pages.
2. Change the year dropdown and confirm the selected-year metric and highlighted bar change.
3. Temporarily rename the CSV to confirm the page reports a missing-data error; restore the filename afterward.
4. Compare the stored CSV's 11 values with the team's shared `corn-production.csv` and the USDA Quick Stats query.
