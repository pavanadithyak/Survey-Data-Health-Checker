# Survey-Data-Health-Checker
# Survey Data Health Checker

A data quality auditing tool that evaluates survey datasets before findings are published.
Flags representation gaps, respondent drift, and class imbalance — then exports a PDF report.

## Problem It Solves
Research firms, polling agencies, and product analytics teams risk publishing biased findings
when survey samples don't reflect the real population. This tool automates the health check
before any report goes live.

## Features
- **Representation Gap** — compares sample demographics vs census benchmarks, flags delta > 5%
- **Respondent Drift** — KS test across time cohorts to detect shifting respondent behavior
- **Class Imbalance** — checks target variable distribution, flags ratio below 0.4
- **Health Score** — single A-D grade summarising all checks
- **Auto PDF Report** — downloadable audit report with charts and flagged issues

## Dataset
Uses UCI Adult (Census Income) dataset via `sklearn.datasets.fetch_openml`.
Swap in any survey CSV by replacing the load step.

## Setup
Run in Google Colab. No local setup needed.

1. Open notebook in Colab
2. Run cells top to bottom
3. PDF auto-downloads on completion

## Tech Stack
- Python, Pandas, NumPy
- SciPy (KS test)
- Scikit-learn (dataset, PCA)
- Matplotlib, Seaborn
- FPDF2 (report generation)

## Output
PDF report containing:
- Representation gap bar charts vs census
- Drift distribution plots per feature
- Class balance chart
- Overall health score and grade

## Use Cases
- Survey research firms validating sample quality
- Product teams auditing user feedback data
- HR teams checking employee survey representation
- Academic researchers verifying dataset integrity
