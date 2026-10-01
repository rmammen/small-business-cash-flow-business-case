# Cash Crunch Alerts: A Small Business Payments Business Case

*A self-directed product case study. All figures not tied to a source below are labeled assumptions for illustration.*

## The problem

Small businesses don't usually fail at the moment they lose money. They get squeezed when cash comes in later than bills go out.

- About **half of small employer firms** reported uneven cash flow as a financial challenge in the past year. The survey counts collecting on receivables as part of this. ([Fed SBCS 2025](https://www.fedsmallbusiness.org/reports/survey/2026/2026-report-on-employer-firms))
- **56%** of firms that applied for financing did it to meet operating expenses, the most common reason given.
- Among firms with financial challenges, the most common responses were using personal funds, raising prices, and drawing down cash reserves. About a quarter made a late payment or skipped one.
- **60%** of firms that borrowed from online lenders said the real cost was higher than they expected.

The pattern: owners find out about a cash gap late, then scramble for whatever money is fastest, often the most expensive option.

## Who it's for

Owners of small employer businesses (roughly 1 to 50 employees) who already use a business credit card and their card issuer's online dashboard, and who don't have a finance team watching cash daily.

**Job to be done:** "Tell me before I'm short on cash, and give me a good way to cover it."

## Competitive landscape

| Product | What it does | Gap |
|---|---|---|
| **QuickBooks Cash Flow Planner** | Forecasts 90 days of cash flow from connected bank accounts and flags upcoming shortfalls | Requires a QuickBooks subscription; the fix (financing, card) happens somewhere else |
| **BILL Cash Flow Forecasting** | Dashboards and what-if forecasts synced from QuickBooks Online | Only on higher-tier plans; built for owners who already use accounting software well |
| **Card issuer and bank dashboards** | Show balances, spending, and past cash flow across business cards, checking, and credit lines | Show what happened; rarely warn about what's coming |

**The opening:** accounting tools can predict a cash crunch but can't solve it in the same place. A business card issuer already holds the card, the line of credit, and the account data, so it can close the loop from warning to action in one screen.

## The proposal

Add **Cash Crunch Alerts** to a business card issuer's small business dashboard: a 30-day forecast built from linked account data that warns owners before a shortfall and offers clear options to handle it.

### Feature prioritization (RICE)

I scored 8 candidate features on Reach, Impact, Confidence, and Effort. Full scoring is in the spreadsheet.

| Rank | Feature | Phase |
|---|---|---|
| 1 | 30-day cash crunch alert from linked accounts | MVP |
| 2 | Plain-language AI explanation of each alert | MVP |
| 3 | Weekly cash flow email digest | MVP |
| 4 | One-tap line of credit draw from the alert | Phase 2 |
| 5 | Suggest paying a supplier by card to extend float | Phase 2 |
| 6 | Overdue-receivable reminder nudges | Phase 2 |
| 7 | What-if planner | Later |
| 8 | Share forecast with accountant | Later |

**Why trust comes before monetization:** the top-ranked features are the ones that make owners believe the forecast. The 2025 SBCS found that accuracy was the top AI concern among firms already using AI. If owners don't trust the alert, they won't act on the financing offer attached to it.

## Opportunity sizing

The model uses three scenarios. Every driver is an editable input in `Cash_Crunch_Alerts_Model.xlsx`.

| | Low | Base | High |
|---|---|---|---|
| Alert adopters | 18,750 | 62,500 | 131,250 |
| Net annual contribution | ($0.67M) | **$1.69M** | $20.1M |
| Payback on build cost | None | **~11 months** | < 1 month |

The customer base is an illustrative assumption (500,000 dashboard users in the base case for a mid-size business card issuer), not company data. The share of customers with cash flow pain comes from the Fed survey.

### What the model taught me

1. **The lending leg alone barely breaks even.** Short draws held for about 3 months earn little per dollar, and in the base case expected credit losses slightly exceed interest and fee revenue. The card float feature and customer retention carry the business case.
2. **Adoption is the swing factor.** The gap between the low and high cases comes mostly from alert adoption and draw rates. That makes the MVP's job clear: prove that owners turn on alerts and act on them.
3. **The low case loses money**, which argues for a small pilot before a full build.

## Risks

- **Forecast accuracy.** A wrong alert erodes trust fast. Mitigation: show confidence ranges and explain each alert in plain language.
- **Responsible lending.** An alert that always leads to a loan offer could push owners into debt they don't need. Mitigation: show non-debt options first (timing payments, collecting receivables) and keep the credit offer clearly optional.
- **Data coverage.** Forecasts are only as good as the accounts owners link. Mitigation: show a data completeness score and prompt owners to link missing accounts.

## Success metrics

- **Adoption:** share of eligible dashboard users who turn on alerts
- **Accuracy:** share of alerted shortfalls that actually happen within 30 days
- **Action rate:** share of alerts followed by an action within 7 days
- **Outcome:** reduction in late payments among alert users versus a holdout group

## Next steps

1. Interview 5 to 10 small business owners to test whether a 30-day warning would change what they do.
2. Prototype the alert screen and test whether owners understand the explanation.
3. Run a pilot with a holdout group to measure real adoption and action rates, then update the model.

## Files

- `README.md`: this business case
- `Cash_Crunch_Alerts_Model.xlsx`: opportunity sizing (3 scenarios), RICE feature prioritization, and sources

## Sources

- Federal Reserve Banks, *2026 Report on Employer Firms: Findings from the 2025 Small Business Credit Survey*
- SBA Office of Advocacy, *Frequently Asked Questions About Small Business 2026*
- Public product pages for QuickBooks Cash Flow Planner and BILL Cash Flow Forecasting
