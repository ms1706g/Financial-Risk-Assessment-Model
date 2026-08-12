# Formula and Methodology Reference

## Core Statement Formulas

- Gross Profit = Revenue - COGS
- EBITDA = EBIT + Depreciation & Amortization
- EBIT = EBITDA - Depreciation & Amortization for projected years
- Net Income = (EBIT - Cash Interest Proxy) * (1 - Tax Rate)
- Total Debt = Commercial Paper + Current Term Debt + Long-Term Debt
- Free Cash Flow = Operating Cash Flow + Capital Expenditure

## Ratio Formulas

- Gross Margin = Gross Profit / Revenue
- EBITDA Margin = EBITDA / Revenue
- EBIT Margin = EBIT / Revenue
- Net Margin = Net Income / Revenue
- ROA = Net Income / Total Assets
- ROE = Net Income / Total Equity
- Current Ratio = Current Assets / Current Liabilities
- Quick Ratio = (Current Assets - Inventory) / Current Liabilities
- Debt / Equity = Total Debt / Total Equity
- Debt / Assets = Total Debt / Total Assets
- Net Debt / EBITDA = (Total Debt - Cash) / EBITDA
- Total Debt / EBITDA = Total Debt / EBITDA
- EBIT / Cash Interest Proxy = EBIT / Cash Interest Proxy
- EBITDA / Cash Interest Proxy = EBITDA / Cash Interest Proxy
- OCF / Debt = Operating Cash Flow / Total Debt
- FCF / Debt = Free Cash Flow / Total Debt

## Risk Scoring

Each major category receives a 1, 2, or 3 score:

- 1 = Strong
- 2 = Moderate
- 3 = Elevated

Weighted score = Profitability Score x 15% + Liquidity Score x 20% + Leverage Score x 25% + Debt Service Score x 25% + Cash Flow Score x 15%

Debt Service uses the EBIT / Cash Interest Proxy score. Cash Flow is scored separately using FCF / Debt, so FCF is not double-counted inside Debt Service.

Risk category:

- <= 1.50 = Low Risk
- > 1.50 and <= 2.25 = Moderate Risk
- > 2.25 = Elevated Risk

The workbook includes checks that total risk weights equal 100% and that final scores remain inside the 1.00 to 3.00 scale.

## Proxy and Projection Limitations

The model uses a cash-interest proxy where a clean standalone interest expense series was not available in the compact source statements. This is an analytical proxy for educational scenario analysis and should not be interpreted as professional credit underwriting.

Projected balance-sheet items use simplified assumptions, including simplified cash, current asset/current liability, inventory, equity, and total asset roll-forwards. These assumptions support scenario analysis only and are not management guidance or professional forecasting.

## What I Need To Learn Before Claiming This Project

- How credit risk differs from market risk, operational risk, and liquidity risk.
- Why underwriting is a formal decision process and why this project is only analytical practice.
- How structured finance differs from corporate credit analysis.
- What an ABS, SPV, securitization, tranche, and waterfall mean.
- Why EBITDA is useful but incomplete without cash flow, capex, working capital, and debt maturity context.
- How real lenders evaluate covenants, collateral, borrower quality, industry risk, management quality, and downside cases.
- Why a model score is not a credit rating.
- Why a cash-interest proxy is not the same as conventional GAAP interest expense.
