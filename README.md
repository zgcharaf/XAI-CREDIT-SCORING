# Explainable Credit Scoring

An exploratory study of interpretable loan-risk segmentation using decision trees. The notebook combines borrower and loan characteristics with interaction features, then translates tree leaves into rules and examines their share of loans and exposure.

**Start here:** [Main notebook](Main_notebook.ipynb).

## What is implemented

- Exploratory distributions, numeric correlations, and categorical associations using Cramér's V.
- Pairwise numeric interactions and ratios, with exploratory Information Value calculations.
- One-hot encoding and a 75/25 random train/test split.
- A decision tree with `max_depth=4` and `min_samples_split=1000`.
- Graphviz visualization and extraction of if–then rules.
- Segment summaries by loan count, loan amount, and adverse outcomes; additional experiments filter rules using exposure and risk constraints.

The notebook treats `loan_status=1` as an adverse outcome in its segment-analysis functions.

## Repository contents

| File | Purpose |
| --- | --- |
| [Main_notebook.ipynb](Main_notebook.ipynb) | Exploratory analysis, model fitting, and segmentation experiments. |
| [credit_risk_dataset.csv](credit_risk_dataset.csv) | Dataset read by the notebook. |
| [config.pkl](config.pkl) | Existing configuration artifact; the inspected notebook does not load it. |

## Open the notebook

```bash
git clone https://github.com/zgcharaf/XAI-CREDIT-SCORING.git
cd XAI-CREDIT-SCORING
python -m venv .venv
# Activate the environment using the command for your operating system.
python -m pip install jupyterlab pandas numpy scipy scikit-learn matplotlib seaborn graphviz
python -m jupyterlab Main_notebook.ipynb
```

Graph rendering also requires the Graphviz system executable. These packages reflect notebook imports; a tested, pinned environment has not yet been supplied.

Keep the CSV in the repository root. The notebook contains exploratory cells that need reordering or repair before a clean run: an early PairGrid cell references `data` and `FULL_Features` before their definitions, and repeated segmentation helpers use global variables.

## Evaluation status

This is a research notebook, not a validated credit decision system. Feature screening is performed before the train/test split, so the held-out split is not independent of feature selection. Segment summaries describe the supplied dataset; they do not establish out-of-sample risk performance.

Priorities for a reproducible benchmark:

1. Fit preprocessing and feature selection on training data only.
2. Consolidate the repeated rule/segment functions and validate rules against tree assignments.
3. Report held-out discrimination, calibration, segment sample sizes, and stability.
4. Document dataset provenance, target meaning, and feature availability at the intended decision time.

No new performance claims are made here.
