# A/B Test Analysis: Free Trial Screener

End-to-end A/B test on a SaaS learning platform's pre-enrollment screener.  
Covers experiment design, statistical testing, and a data-driven launch decision.

## The experiment
A screener was shown to users after clicking "Start Free Trial" asking how many hours/week they could commit. Users below 5 hours/week were redirected to free materials. The question: does filtering low-commitment users improve paid conversion?

## Key result
| Metric | Control | Experiment | Δ | Significant? |
|--------|---------|------------|---|-------------|
| Gross Conversion | 21.9% | 19.8% | -2.06pp | ✅ Yes |
| Net Conversion | 11.8% | 11.3% | -0.49pp | ❌ No |

**Recommendation: Do not launch.** The screener reduced enrollment without improving payment rates.

## What's in this repo
- `ab_test_analysis.ipynb` — full analysis: sanity checks, z-test, confidence intervals, visualizations
- `ab_test_summary.pdf` — one-page summary: hypothesis, method, results, recommendation
- `data/` — raw control and experiment CSVs

## Stack
Python · pandas · scipy · statsmodels · matplotlib · seaborn · fpdf2
