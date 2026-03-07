# Should You Buy? — Singapore Property Decision Tool

A free, open-source tool that helps Singaporeans figure out whether buying a home makes financial sense compared to renting or waiting. It runs year-by-year wealth projections across multiple paths and shows which one leaves you wealthiest.

**[Use the tool](https://l-t-x-o.github.io/should-you-buy-sg/)** | **[Give feedback](https://forms.gle/QDU2FmEUkWHw9nEy6)** | **[Buy me an iTea](https://buymeacoffee.com/ltxo)**

![Results screenshot](og-image.png)

## What it does

The tool compares up to four paths side by side: staying with parents and investing, renting and investing the difference, buying a resale HDB, or buying a private condo (resale, new launch, or balance unit). Each path is simulated year by year, accounting for salary growth, expense inflation, rent escalation, mortgage payments, CPF contributions, property appreciation, lease depreciation, investment compounding, and portfolio allocation between equities and bonds.

## Key features

The tool includes a comparison matrix showing all paths side by side across every key metric, a year-by-year wealth trajectory chart, sensitivity analysis that shows which path wins at different market returns and holding periods, and a plain English explanation of results written for people who are not finance professionals.

Additional capabilities include the ability to paste text from a PropertyGuru or 99.co listing to auto-populate property fields, an ETF selector with historical returns for popular Singapore-accessible funds, a buy-to-rent scenario where you purchase property and rent it out (with non-owner-occupied property tax and HDB MOP restrictions), CPF housing grant support for HDB (up to S$80,000 for first-timer couples), an equity/bond portfolio split with SSB yield modeling, a configurable investment rate (what % of surplus you actually invest), TDSR and MSR regulatory checks, a liquid vs non-liquid wealth breakdown, and a singles-under-35 HDB restriction check.

All defaults are set to Singapore medians. Runs entirely client-side with no data sent anywhere. No sign-up needed.

## How to use

Open the tool in any modern browser. Walk through 4 steps of inputs (your profile, alternatives, properties, and assumptions), then view the results. Takes about 3 minutes. For the property step, you can paste text directly from a PropertyGuru or 99.co listing to auto-populate fields.

## Singapore-specific modeling

BSD using current progressive tiers. ABSD rates for SC, SPR, and foreigners (post-April 2023). SSD for private property sold within 3 years. CPF OA contribution rates by age bracket with the S$8,000 salary cap. CPF accrued interest at 2.5%. HDB lease depreciation factors and CPF age-plus-lease eligibility rules. Owner-occupied and non-owner-occupied property tax rates from the IRAS progressive schedule. HDB loan (80% LTV, 0% min cash) vs bank loan (75% LTV, 5% min cash). 5-year MOP enforcement for HDB paths. CPF housing grants for eligible buyers.

## Assumptions and limitations

This is a decision-support tool, not financial advice. Property appreciation is modeled as a constant annual rate rather than cyclically. Investment returns assume a constant annual rate. The model does not account for income tax on rental income. CPF Special Account, Medisave, and retirement sum interactions are not modeled. BTO flats are not modeled due to unpredictable ballot timelines. The tool does not weigh lifestyle value, emotional stability, or other non-financial factors.

## Technical details

Single HTML file, no build step, no dependencies, no frameworks. Vanilla JavaScript with a custom canvas-based charting engine. All calculations run client-side.

## License

MIT

