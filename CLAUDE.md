# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Singapore property buy-vs-rent decision tool. Single-page web app that runs year-by-year wealth projections comparing up to four paths: stay with parents, rent, buy resale HDB, or buy private condo. Hosted on GitHub Pages at `l-t-x-o.github.io/should-you-buy-sg/`.

## Development

No build step, no dependencies, no frameworks. Open `index.html` directly in a browser to run. `should-you-buy-sg.html` is an identical copy of `index.html`.

## Architecture

Everything lives in a single `index.html` file (~1028 lines) containing CSS, HTML, and JavaScript inline.

### Structure within the file

1. **CSS** (lines ~19-650): Custom design system using CSS variables in `:root`. Two font families: Fraunces (display) and Outfit (body). Responsive with mobile breakpoints at 520px.

2. **Calculation engine** (first `<script>`, lines ~651-783): Pure functions wrapped in an IIFE that exposes `window.Calc`. Key functions:
   - `simProperty(kind, prop, inp)` — core simulation for HDB/private property paths
   - `simWait(inp)` / `simRent(inp)` — simulation for non-property paths
   - `compare(inp)` — runs all simulations, computes break-even appreciation, sensitivity analysis
   - `runSens(inp)` / `qc(inp)` — sensitivity grid across market returns and holding periods
   - `quickFeasibility(kind, inp)` — lightweight check for real-time UI feedback
   - Financial primitives: `bsd()`, `absdRate()`, `ssdRate()`, `pmt()`, `loanBal()`, `fv()`, `cpfOARate()`, `hdbLF()`, `privLF()`, `calcPropTax()`

3. **UI layer** (second `<script>`, lines ~785-end): 4-step wizard flow + results view. Key areas:
   - `readState()` — collects all form inputs into the `inp` object consumed by the calc engine
   - `renderResults()` — builds results HTML including chart, comparison matrix, sensitivity table
   - `drawChart()` — custom canvas-based charting (no library)
   - `parseListing()` — extracts property details from pasted PropertyGuru/99.co listing text
   - Preset system (`PRESETS` object) for cautious/base/optimistic assumption bundles

### Data flow

User inputs (wizard steps 1-4) -> `readState()` builds `inp` object -> `Calc.compare(inp)` runs all simulations -> `renderResults()` draws output. No state management library; DOM is the source of truth for inputs.

## Singapore-Specific Logic

The calculation engine encodes current Singapore tax and regulatory rules: BSD tiers, ABSD rates (post-April 2023), SSD rates, CPF OA contribution rates by age bracket (capped at S$8,000), CPF accrued interest at 2.5%, HDB lease depreciation factors, owner-occupied property tax (IRAS progressive rates), HDB vs bank loan parameters (LTV, minimum cash), and 5-year MOP. Changes to these rules require updating the corresponding pure functions in the calc engine.
