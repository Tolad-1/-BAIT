# AI Log — MPFN Corn Sourcing Dashboard

**Project:** Harvest to Screen: Build an Ag Data Web Page  
**AI Tool:** ChatGPT  
**Data Source:** USDA NASS Quick Stats  
**Decision Question:** Based on historical Minnesota corn production, should MPFN plan for tighter ingredient sourcing conditions in the upcoming production year?

## 1. Initial Dashboard Development

I asked ChatGPT to create an HTML dashboard using Minnesota corn production data from USDA NASS. The dashboard needed a year filter, an interactive chart, and comments explaining the data source and storage.

ChatGPT initially created a dashboard that loaded production data from a separate CSV file.

Prompts:
You are a supply chain and data analytics tutor for college students. I am a student in a digital supply chain class. This is my assignment meant for use of AI and github, including the rubric:
I approve Option A. Use the verified USDA annual SURVEY production totals from 2015–2025. Walk me through building the HTML dashboard step by step.
My HTML dashboard opens, but the CSV data does not load. Walk me through troubleshooting it.
I've uploaded my dashboard files to my GitHub student folder. Help me test the website using GitHub Pages.
Go back to step 3 of building first draft with LLM. Do this: Build one self-contained HTML file that answers this question for a Minnesota agriculture supply chain:

## 2. Data Verification

I worked with ChatGPT to identify the appropriate USDA records for the analysis. We selected annual SURVEY production totals for Minnesota corn for grain, covering 2015–2025.

The original dataset contained additional records, including monthly forecasts and other categories, which could cause double-counting if combined incorrectly.

## 3. Error and Troubleshooting

**Problem:** The HTML dashboard opened in my browser, but the CSV data did not load.

**Investigation:** I asked ChatGPT to help troubleshoot the problem. We identified that opening an HTML file directly through a `file:///` address can prevent JavaScript from loading a separate CSV because of browser security restrictions.

**Correction:** I requested a self-contained HTML dashboard. ChatGPT embedded the verified USDA production data directly into the HTML file, removing the need to load an external CSV when opening the page.

## 4. Testing and Verification

I opened the revised HTML dashboard and reviewed its appearance.

The dashboard was designed to show annual production values, including:

- 2023: 1,513,300,000 bushels
- 2024: 1,345,020,000 bushels
- 2025: 1,696,440,000 bushels

These values were used as reference points for checking the dashboard against the USDA dataset.

## 5. Code Reading

I located the `annualProduction` variable and added three comments beginning with `// ME:`.

The comments explain where the data originates, where it is stored in the browser, and how the selected year changes the displayed results.

## 6. AI Limitations and Lessons Learned

The biggest lesson was that generating HTML code does not guarantee the data will load correctly.

I also learned that USDA datasets can contain multiple reporting categories, so filtering records correctly is important before using the numbers to support a supply chain decision.

The final dashboard uses stored historical data rather than relying on a live USDA connection.
