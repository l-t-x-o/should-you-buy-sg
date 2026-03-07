# Should You Buy? — Singapore Property Decision Tool

A free, open-source tool that helps Singaporeans compare buying property against renting or waiting. It runs year-by-year wealth projections across multiple paths and shows which one leaves you wealthiest at the end of your chosen time horizon.

**[Use the tool](https://l-t-x-o.github.io/should-you-buy-sg/)**

![Results screenshot](og-image.png)

## What it does

The tool compares up to four paths side by side: staying with parents and investing everything, renting and investing the difference, buying a resale HDB, or buying a private condo (resale, new launch, or balance unit). For each path, it simulates wealth year by year, accounting for salary growth, expense inflation, rent escalation, mortgage payments, CPF contributions, property appreciation, lease depreciation, and investment compounding.

## Features

The tool includes a year-by-year wealth trajectory chart, a side-by-side comparison matrix, and sensitivity analysis that shows which path wins at different market returns and holding periods. You can paste text from a PropertyGuru or 99.co listing to auto-extract price, lease, rent, and fees. An ETF selector lets you anchor your return assumption to real historical data from popular Singapore-accessible funds like VWRA, IWDA, CSPX, and ES3. TDSR and MSR regulatory checks flag loans that would be rejected. Break-even appreciation shows the minimum property growth needed to beat investing. Property tax is auto-calculated from estimated Annual Value using IRAS progressive rates. New launch and balance unit paths model the bridge rental cost during the wait for TOP. All defaults are set to Singapore medians.

Runs entirely client-side. No data is sent anywhere. No sign-up needed.

## How to use

Open the tool in any modern browser. Walk through 4 steps of inputs (your profile, alternatives, properties, and assumptions), then view the results. Takes about 3 minutes. All inputs have sensible defaults based on Singapore medians. Tooltips explain what each field means and what range is typical.

## Singapore-specific modeling

The engine models BSD using current progressive tiers, ABSD rates for SC, SPR, and foreigners (post-April 2023), SSD for private property sold within 3 years, CPF OA contribution rates by age bracket with the S$8,000 salary cap, CPF accrued interest at 2.5%, HDB lease depreciation factors and CPF age-plus-lease eligibility rules, owner-occupied property tax rates from the IRAS progressive schedule, HDB loan (80% LTV, 0% min cash) vs bank loan (75% LTV, 5% min cash), and 5-year MOP enforcement for HDB paths.

## Assumptions and limitations

This is a decision-support tool, not financial advice. Property appreciation is modeled as a constant annual rate rather than cyclically. Investment returns assume a constant annual rate. The model does not account for rental income if the property is let out. CPF Special Account, Medisave, and retirement sum interactions are not modeled. The tool does not weigh lifestyle value, emotional stability, or other non-financial factors.

## Technical details

Single HTML file, no build step, no dependencies, no frameworks. Vanilla JavaScript with a custom canvas-based charting engine. All calculations run client-side. The file can be opened directly in a browser or hosted on any static file server.

## License

MIT
