# Should You Buy? — Singapore Property Wealth Projection Tool

What does the math actually say? Property, stocks, bonds, or some combination? This is a first-pass scenario calculator for straightforward Singapore home-buying cases.

**[Run the numbers](https://l-t-x-o.github.io/should-you-buy-sg/)** | **[Give feedback](https://forms.gle/QDU2FmEUkWHw9nEy6)** | **[Donate to SPCA](https://portal.spca.org.sg/Donation/DonateNow)**

![Results screenshot](og-image.png)

## What it does

Compare staying with parents and investing, renting and investing the difference, buying a resale HDB, or buying a private condo. Each path is simulated year by year with salary growth, expense inflation, rent escalation, mortgage payments, CPF, property appreciation with lease depreciation, and a blended equity/bond investment portfolio. The tool recommends the best affordable path and flags if an unaffordable option would have projected higher.

## Regulatory modeling (as of July 2025)

BSD using current progressive tiers. ABSD rates for SC, SPR, and foreigners (post-April 2023). SSD using the 4-year schedule at 16/12/8/4% (effective 4 July 2025). CPF OA contribution rates by age with S$8,000 salary cap and 2.5% accrued interest. HDB lease depreciation factors. Property tax using the IRAS 2025 progressive schedule for both owner-occupied (first S$12,000 at 0%) and non-owner-occupied (12/20/28/36%). HDB loan at 75% LTV (updated August 2024) with 0% min cash. Bank loan at 75% LTV with 5% min cash. TDSR stress-tested at 4% floor for bank loans. MSR stress-tested at 3% floor for HDB loans. 5-year MOP enforcement. Singles under 35 blocked from HDB (infeasible, not just warned).

## Key features

Side-by-side comparison matrix. Year-by-year wealth chart (infeasible paths as dashed lines). Unemployment stress test (months at zero income, color-coded). Interest rate sensitivity (+1%, +2%). SSD early exit penalty table. Break-even appreciation benchmarked against best available non-buy path. Quick-adjust on results page. Save link or share results summary. PSF calculator. New launch premium warning. Agent commission transparency note. CPF housing grants (up to S$120,000 EHG). Buy-to-rent with 15% rental income haircut for vacancy and costs. ETF selector with real 10-year returns. Separate equity/bond return inputs.

## What this tool is NOT

This is not a loan-approval, tax, or legal eligibility engine. It does not handle mixed-citizenship couples, separate CPF balances, outstanding housing loan LTV variants, EC purchases, FTA-qualifying foreigners, or BTO ballot timelines. It models one household making one property decision in straightforward cases.

## Built with

Claude, a spreadsheet, and too much bubble tea. By Leonard, a regular Singaporean figuring it out like the rest of us.

## License

MIT
