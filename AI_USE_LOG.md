# AI Use Log — Data Science Assignment 5

**Student:** Amsalu Tessema Adgeh  
**Student ID:** 2026A8000929002

## Tool and tasks
For prepared this assignment such as for code problem fixing and optimazation as well as report preparation to interpretat the result, I used Deepseek, Perplexity, and Claude AI was used to help: 
(1) identify a genuine public time-series dataset and locate its official repository record; 
(2) draft a reproducible notebook structure; 
(3) propose chronological rolling-origin evaluation, causal lag features, leakage assertions, metrics, drift diagnostics, and a monitoring/fallback plan; and 
(4) draft documentation and a reproducibility checklist.

## Advice accepted
- Use the UCI Individual Household Electric Power Consumption dataset and cite its DOI and CC BY 4.0 license.
- Aggregate minute-level active power to hourly means; predict the next hourly bin.
- Use persistence and 24-hour seasonal-naive baselines plus a learned model.
- Use expanding chronological origins and refit imputation/scaling/model inside each origin.
- Exclude same-hour sensor values from predictors and shift target-derived features to past observations.
- Export raw predictions, metrics, diagnostics, data hash, and environment provenance.

## Advice rejected / constrained
- No fabricated metric, result, successful execution, GitHub URL, commit, or tag was accepted.
- No future or same-hour measurements are used as forecast-time features.
- No random train/test split is used for the time-series evaluation.

## Independent verification required from student
- Run the notebook from a clean environment and inspect the data parsing, archive hash, number of valid hourly bins, six origin boundaries, and leakage assertions.
- Verify the actual metric tables and plots against `rolling_predictions_raw.csv`.
- Confirm the UCI source, citation, and license.
- Validate the hourly availability/ingestion assumption; the UCI documentation does not specify real-time latency.
- Review and edit the analysis and DS-Ass5.pdf report result summary which is already uploaded to Drive and share with your account, based on the actual run.