# Audit Report - Financial Risk Assessment & Scenario Analysis Model

## A. Issues Found

- Financial Statements had row-alignment errors: Gross Margin showed Gross Profit values, Operating Expenses showed margin percentages, and projected Inventory/Current Liabilities were swapped.
- Scenario weighted score helper double-counted Cash Flow inside Debt Service by combining the 25% Debt Service weight with the 15% Cash Flow weight in one row.
- Debt-service terminology used "Interest Coverage" even though the denominator is a cash-interest / near-term payment proxy, not a clean conventional GAAP interest expense series.
- Sensitivity table formulas were not useful: the EBIT / coverage proxy side returned zeros because percentage headers were text labels, and the risk-score sensitivity output was effectively static.
- Data-quality checks showed OK but did not include explicit PASS/FAIL checks for 100% risk weights or score-range validity.
- README and methodology needed clearer documentation of the cash-interest proxy and simplified balance-sheet projection assumptions.

## B. Fixes Applied

- Corrected Financial Statements row formulas and labels so source data, calculated rows, and projection rows align with their stated line items.
- Renamed the debt-service metric consistently to "EBIT / Cash Interest Proxy" and "EBITDA / Cash Interest Proxy" where applicable.
- Corrected scenario scoring so the overall score equals:

  Profitability x 15% + Liquidity x 20% + Leverage x 25% + Debt Service x 25% + Cash Flow x 15%

- Separated Debt Service scoring from Cash Flow scoring. Debt Service now uses the EBIT / Cash Interest Proxy score; Cash Flow separately uses FCF / Debt.
- Added visible model checks for total risk weights = 100%, overall score range, and scenario score range.
- Reworked the sensitivity table so revenue growth and EBITDA margin assumptions affect EBIT / Cash Interest Proxy and risk-score outputs.
- Updated workbook README, project README, and methodology documentation to explain the proxy limitation and simplified projection assumptions.

## C. Formulas / Logic Changed

- Gross Margin = Gross Profit / Revenue.
- Operating Expenses = Gross Profit - EBIT for historical years; projected years use Gross Profit - EBIT.
- EBITDA = EBIT + Depreciation & Amortization.
- EBIT = EBITDA - Depreciation & Amortization.
- Cash Interest Proxy is a separate debt-service denominator and is not labeled as conventional interest expense.
- Current Liabilities projection = Current Assets / selected scenario Current Ratio.
- Inventory projection = Current Assets x 2025 inventory/current-assets ratio.
- Scenario Overall Risk Score = SUM(weighted category scores).
- Scenario Debt Service weighted score = 25% x EBIT / Cash Interest Proxy score.
- Scenario Cash Flow weighted score = 15% x FCF / Debt score.

## D. Remaining Limitations

- This remains a compact educational model, not a full three-statement model.
- Balance-sheet projections are simplified and should not be treated as professional forecasts or management guidance.
- The cash-interest proxy is useful for educational scenario analysis but is not the same as a clean GAAP interest expense series.
- The thresholds and weights are illustrative portfolio-model assumptions, not rating-agency criteria or JPMorgan methodology.
- The model does not include covenants, debt maturities, collateral analysis, ABS waterfalls, tranche analysis, peer benchmarking, or management due diligence.

## E. What I Should Understand Before Using This On My Resume

- Why the model uses a cash-interest proxy and how that differs from conventional interest expense.
- How each ratio is calculated and which financial statement line drives it.
- Why FCF / Debt must be treated as a cash-flow metric, not double-counted inside Debt Service.
- How scenario assumptions flow into revenue, EBITDA, EBIT, FCF, leverage, debt-service proxy coverage, and the risk score.
- Why the output is an illustrative risk assessment, not an official credit rating or underwriting decision.
- Why simplified balance-sheet assumptions are acceptable here only because the model is positioned as a learning/portfolio project.

## F. Resume Safety Assessment

Yes. The corrected project is safe to describe as an "Excel-based Financial Risk Assessment & Scenario Analysis Model" as long as it is not described as credit underwriting, structured finance execution, ABS underwriting, investment banking experience, credit approval work, or JPMorgan methodology.
