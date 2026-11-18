# MPFN Minnesota Corn Sourcing Signal

**Decision question:** Based on historical Minnesota corn production, should MPFN plan for tighter ingredient sourcing conditions in the upcoming production year?

**Source:** USDA NASS Quick Stats: https://quickstats.nass.usda.gov/results/EE31286B-22C5-3414-AE4C-E855D535F1F1

**Data:** `corn-production.csv` contains the 11 annual records (2015–2025) selected from the uploaded 174-record USDA CSV with Program=SURVEY, Domain=TOTAL, Period=YEAR, Geo Level=STATE, State=MINNESOTA, Data Item=CORN, GRAIN - PRODUCTION, MEASURED IN BU. Dataset supplied to this project on November 17, 2026; verify original download date.

**How to view:** Host this folder with GitHub Pages or run `python -m http.server 8000` in this folder, then open http://localhost:8000/. Browsers often block `fetch()` for local `file://` URLs.

**Interpretation:** The chart compares statewide production with the 2015–2025 average. It does not establish ingredient availability, future production, or prices.
