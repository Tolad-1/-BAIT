# Minnesota Corn Sourcing Signal

**Decision question:** Should BAIT flag potential corn-sourcing pressure for its next planning cycle based on Minnesota's latest reported corn-for-grain production compared with the previous ten-year average?

**Data source:** USDA National Agricultural Statistics Service (NASS), Quick Stats.  
**USDA query:** https://quickstats.nass.usda.gov/results/EE31286B-22C5-3414-AE4C-E855D535F1F1  
**Fields:** Year, Data Item, Value (normalized as `production_bu`), Geography.  
**Coverage:** Minnesota state-level corn-for-grain production, 2015–2025.  
**Local data copy:** `corn-production.csv`. Downloaded from the team's shared CSV on November 19, 2026. The shared CSV was committed November 17, 2026; its original USDA extraction date was not documented.

## How to run
Keep `index.html` and `corn-production.csv` in the same folder. Because browsers commonly block `fetch()` from a `file://` address, run a local server from this folder:

```bash
python -m http.server 8000
```

Then open http://localhost:8000 in a browser. The page also works when the folder is hosted with GitHub Pages.

## Interpretation and limitations
The dashboard compares each selected year with the 2015–2024 average. It is a historical statewide production signal only. It does not measure available inventory, local supplier capacity, prices, future production, or BAIT's actual demand. Use it to prompt supplier conversations alongside other information, not as a stand-alone purchasing instruction.
