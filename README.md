# Financial Risk Assessment & Scenario Analysis Model

Educational portfolio project analyzing Apple Inc. public annual financial statements with a transparent Excel-based risk model.

## Problem Statement

A risk analyst needs to understand whether a company has enough profitability, liquidity, leverage capacity, debt-service cushion, and free cash flow to remain resilient when business conditions deteriorate.

## Objective

Build a compact, explainable model that demonstrates financial statement analysis, ratio analysis, risk-driver identification, scenario analysis, sensitivity analysis, and data-quality checks.

## Dataset

The workbook uses Apple Inc. annual financial statement data in USD millions for FY2021-FY2025. Historical actuals are sourced from Apple SEC Form 10-K filings. Debt-service analysis uses a cash-interest / near-term payment proxy where a clean standalone interest expense series was not available in the compact source statements.

Sources:

- Apple FY2025 Form 10-K: https://www.sec.gov/Archives/edgar/data/320193/000032019325000079/aapl-20250927.htm
- Apple FY2024 Form 10-K: https://www.sec.gov/Archives/edgar/data/320193/000032019324000123/aapl-20240928.htm
- Apple FY2022 Form 10-K: https://www.sec.gov/Archives/edgar/data/320193/000032019322000108/aapl-20220924.htm

## Methodology

1. Link historical actuals from Raw Data into Financial Statements.
2. Calculate margins, leverage, liquidity, debt-service, and cash-flow ratios.
3. Apply illustrative risk thresholds that are documented in the Assumptions sheet.
4. Use Base, Downside, and Stress cases to change revenue growth, EBITDA margin, cash-interest proxy, debt, capex, operating cash flow, and current ratio.
5. Generate a weighted risk score using formula-driven category scores.
6. Identify risk drivers only when the underlying metric crosses a threshold.

## Financial Metrics

Key outputs include gross margin, EBITDA margin, EBIT margin, net margin, ROA, ROE, current ratio, quick ratio, debt/equity, debt/assets, net debt/EBITDA, total debt/EBITDA, EBIT / Cash Interest Proxy, EBITDA / Cash Interest Proxy, OCF/debt, free cash flow, and FCF/debt.

## Risk Framework

The model uses illustrative portfolio-model assumptions:

- Profitability: 15%
- Liquidity: 20%
- Leverage: 25%
- Debt Service: 25%
- Cash Flow: 15%

The output is Low Risk, Moderate Risk, or Elevated Risk. It is not an official credit rating.

Weighted score = Profitability x 15% + Liquidity x 20% + Leverage x 25% + Debt Service x 25% + Cash Flow x 15%. The workbook includes a visible check that total risk weights equal 100%.

## Scenario Analysis

Base Case keeps growth and margins resilient. Downside Case reduces revenue growth and margins while increasing debt and the cash-interest proxy. Stress Case applies a sharper revenue decline, lower EBITDA margin, higher debt, higher capex intensity, weaker OCF margin, and lower current ratio.

## Key Findings

In the historical period, Apple shows very strong profitability and free cash flow generation, with manageable leverage relative to EBITDA. The model also highlights why liquidity and trend context matter: current ratio can be below 1.0x even when the company has meaningful operating cash flow and marketable securities. Under stress assumptions, risk increases because EBITDA, free cash flow coverage, and EBIT / Cash Interest Proxy deteriorate while debt rises.

## Limitations

This project is not professional credit underwriting, investment advice, investment banking work, structured finance execution, ABS underwriting, real-world credit approval experience, or a representation of JPMorgan's internal risk methodology. It does not include covenant analysis, rating-agency methodology, collateral waterfall modeling, loan tape analysis, industry peer benchmarking, or management due diligence.

Projected balance-sheet items use simplified assumptions for educational scenario analysis. They should not be interpreted as management guidance or professional forecasting.

The model uses a cash-interest proxy where a clean standalone interest expense series was not available in the compact source statements. This is an analytical proxy for educational scenario analysis and should not be interpreted as professional credit underwriting.

## Interview Talking Points

- I built a transparent Excel model using public 10-K data.
- I separated historical actuals, assumptions, and forecast/scenario outputs.
- I calculated profitability, liquidity, leverage, debt-service, and cash-flow ratios.
- I used a rule-based risk framework and clearly labeled it as illustrative.
- I tested how downside assumptions affect risk indicators.
- I included data-quality checks and avoided presenting the project as underwriting experience.

## Resume Bullets

- Built an Excel-based financial risk assessment model using public Apple financial statements to calculate profitability, liquidity, leverage, debt-service, and cash-flow ratios with formula-driven risk flags and data-quality checks.
- Developed Base, Downside, and Stress scenario analysis plus sensitivity tables to evaluate how changes in revenue growth, EBITDA margin, debt, cash-interest proxy, capex, and operating cash flow affect overall financial risk.
