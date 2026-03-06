# Should You Buy? — Singapore Property Decision Tool

A free, open-source tool that helps Singaporeans compare buying property against renting or waiting. It runs year-by-year wealth projections across four paths and shows which one leaves you wealthiest at the end of your chosen time horizon.

![Results screenshot](og-image.png)

## What it does

The tool compares four paths side by side:

- **Stay with parents + invest** — live at low cost and put everything into the market
- **Rent + invest the difference** — rent a place and invest what you would have spent on a mortgage
- **Buy a resale HDB** — purchase public housing with HDB or bank loan
- **Buy a private condo** — purchase private property (resale, new launch, or balance unit)

For each path, it simulates wealth year by year, accounting for salary growth, expense inflation, rent escalation, mortgage payments, CPF contributions, property appreciation, lease depreciation, and investment compounding.

## Features

- Year-by-year wealth trajectory chart across all four paths
- TDSR and MSR regulatory checks (flags loans that would be rejected)
- Sensitivity analysis: see which path wins at different market returns and holding periods
- Break-even appreciation: the minimum property growth needed to beat investing
- Auto-calculated property tax from estimated Annual Value
- New launch and balance unit support with bridge rental modeling
- Three scenario presets (Cautious, Base case, Optimistic) to stress-test results
- Runs entirely client-side. No data is sent anywhere.

## How to use

Open the tool in any modern browser. Walk through 4 steps of inputs (your profile, alternatives, properties, and assumptions), then view the results. Takes about 3 minutes.

All inputs have sensible defaults. Tooltips explain what each field means and what range is typical.

## Singapore-specific modeling

- BSD (Buyer's Stamp Duty) calculated using current progressive tiers
- ABSD (Additional Buyer's Stamp Duty) rates for SC, SPR, and foreigners (post-April 2023)
- SSD (Seller's Stamp Duty) for private property sold within 3 years
- CPF OA contribution rates by age bracket, with salary cap at S$8,000
- CPF accrued interest at 2.5%
- HDB lease depreciation factors and CPF age-plus-lease eligibility rules
- Owner-occupied property tax rates from IRAS progressive schedule
- HDB loan (80% LTV, 0% min cash) vs bank loan (75% LTV, 5% min cash)
- 5-year MOP enforcement for HDB paths

## Assumptions and limitations

This is a decision-support tool, not financial advice. Key limitations:

- Property appreciation is modeled as a constant annual rate. In reality, property markets are cyclical.
- Investment returns assume a constant annual rate. Actual returns vary significantly year to year.
- The model does not account for rental income if the property is let out.
- CPF Special Account, Medisave, and retirement sum interactions are not modeled.
- The tool does not weigh lifestyle value, emotional stability, or other non-financial factors.

## Technical details

Single HTML file, no build step, no dependencies, no frameworks. Vanilla JavaScript with a custom canvas-based charting engine. All calculations run client-side. The file can be opened directly in a browser or hosted on any static file server.

## License

MIT
