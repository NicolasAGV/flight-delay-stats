# Flight Delay Stats

Applied statistics on BigQuery's public `airline_ontime_data.flights` dataset (~69M US domestic flights, 2002–2012).

Goal: practice using statistical reasoning — not just descriptive summaries — to investigate real data, question assumptions, and avoid misleading conclusions.

## What's inside

- **Distribution & skew** — comparing mean vs. median, Pearson's skewness coefficient, and why average delay alone is a misleading headline number
- **Data quality investigation** — tracing extreme outlier values to a midnight-rollover calculation bug in the source data, verified at the row level
- **Outlier detection** — IQR-based fences on a skewed distribution
- **Confidence intervals & hypothesis testing** — comparing two airlines' average delay on the same route, with results from two different time windows (one significant, one not)
- **Coefficient of variation** — comparing delay predictability across months, independent of each month's average delay level
- **Correlation vs. causation** — testing (and rejecting) a specific hypothesis about whether short delays get "made up" in flight

## Tools

BigQuery (SQL) for aggregation, Python (pandas, scipy, matplotlib) for analysis and visualization.

## Notes

Queries are written to pull pre-aggregated results from BigQuery rather than raw rows, keeping the analysis fast and cheap to run.
