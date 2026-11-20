## Canvas reflection draft (about 250 words)

The biggest thing I had to pay attention to was how the data was formatted and where the webpage was getting it from. The shared USDA CSV had production numbers with commas inside quotation marks, such as 1,428,800,000. That is normal CSV formatting, but a basic script that splits every row at each comma can read the number incorrectly. I checked the original rows and saved a cleaned copy with the production values as plain numbers. I also learned that a webpage opened directly as a file may not be able to load a separate CSV because of browser security rules, so it needs to run through GitHub Pages or a local web server.

The data now lives in my project folder in `corn-production.csv`. The webpage reads that saved copy, so it does not need the USDA website to be online every time someone opens it. Someone who can edit my GitHub repository could replace the CSV or change the code without me knowing, so the file's source, date, and commit history matter.

A downstream person who could use this signal is someone responsible for purchasing or supplier planning. They could use a change in Minnesota corn production as a reason to contact suppliers and ask about availability, but they would need trustworthy USDA data, a clear time period, and an explanation of what the numbers do and do not measure. Statewide production alone does not prove that corn is scarce or that prices will rise.

For the BAIT storefront to trust this signal next week, it would need to store the date the data was last updated, along with the source and the exact reporting period. That would help users tell whether they are making a decision from current information or an old snapshot.
