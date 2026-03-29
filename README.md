# Data Analytics Best Practice

Reusable notebooks for common structured-data case studies, from general analysis to modeling, experimentation, and forecasting.

## Project Purpose

This repository is designed as a starter kit for data analytics case studies based on structured tabular data.

The notebooks are intentionally split by use case so you can pick the one that matches the assignment instead of forcing every workflow into a single file.

## Files

- `data_case_study.ipynb`
  General-purpose notebook for most analytics case studies. Use this for loading data, data quality checks, cleaning, feature preparation, exploratory data analysis, and simple business insights.

- `customer_segmentation_clustering.ipynb`
  Notebook for unsupervised customer segmentation. Includes feature preparation, clustering model comparison, PCA-based 2D and 3D visualization, and cluster profiling.

- `regression_modeling.ipynb`
  Notebook for continuous-target prediction tasks on structured data. Covers baseline regression models, random forest, XGBoost, model comparison, and SHAP-based feature interpretation.

- `classification_modeling.ipynb`
  Notebook for labeled classification tasks on structured data. Covers binary and multiclass classification with baseline models, random forest, XGBoost, and an optional RNN scaffold for true sequence data.

- `experimentation_causal_inference.ipynb`
  Notebook for causal and impact analysis. Includes A/B test style evaluation, Difference-in-Differences, and propensity score weighting.

- `time_series_forecasting.ipynb`
  Notebook for forecasting over time. Includes a simple baseline model, ARIMA, SARIMA, and optional deep-learning scaffolds for LSTM and Transformer-based approaches.

- `requirements.txt`
  Python dependencies used by the notebooks.

- `.gitignore`
  Ignore rules for virtual environments, notebook checkpoints, cache files, and local Jupyter state.

- `.vscode/settings.json`
  Workspace settings so VS Code uses the local `.venv` interpreter and runs notebooks with a local Jupyter server.

- `.vscode/extensions.json`
  Recommended VS Code extensions for Python and Jupyter.

## Recommended Usage

- Use `data_case_study.ipynb` for most standard case studies on CSV or similar tabular datasets.
- Use `customer_segmentation_clustering.ipynb` when the goal is segmentation without a labeled target.
- Use `regression_modeling.ipynb` when the task is continuous-value prediction, sales driver analysis, or regression model comparison.
- Use `classification_modeling.ipynb` when the task is binary or multiclass prediction.
- Use `experimentation_causal_inference.ipynb` when the task is treatment effect estimation or uplift analysis.
- Use `time_series_forecasting.ipynb` when the task is forecasting with timestamped data.

## Supported Environments

These notebooks are standard `.ipynb` files and can be used in:

- VS Code
- Jupyter Notebook
- JupyterLab
- Google Colab

## Local Setup

If you want to run the notebooks locally, a simple setup is:

1. Open this folder in your preferred local environment.
2. Open a terminal.
3. Create a virtual environment:

```bash
python3 -m venv .venv
```

4. Activate it:

```bash
source .venv/bin/activate
```

5. Install dependencies:

```bash
python -m pip install -r requirements.txt
```

6. Open the notebook you want to use.
7. Select the Python kernel from `.venv`.
8. Run the notebook cells from top to bottom.

## VS Code Notes

If you use VS Code:

- install the Python extension
- install the Jupyter extension
- the workspace includes `.vscode/settings.json` so the local `.venv` interpreter is selected more easily

## Colab Notes

If you use Google Colab:

- upload the notebook file to Colab, or open it from GitHub
- upload your dataset manually, or mount Google Drive and update `DATA_PATH`
- install any missing packages inside Colab if needed

Example:

```python
!pip install -r requirements.txt
```

## Data Input

The notebooks default to:

```python
DATA_PATH = Path('data.csv')
```

This repository does not include a sample dataset by default.

Before running a notebook, do one of these:

- place your own `data.csv` file in the project root, or
- update `DATA_PATH` inside the notebook to point to your dataset

## Notes

- These notebooks are designed primarily for structured data, not NLP, computer vision, or recommender-system case studies.
- Some advanced sections, such as XGBoost, SHAP, LSTM, and Transformer examples, may require additional setup time or heavier dependencies.
- Deep learning sections are included as optional scaffolds, not as the default recommendation for ordinary tabular case studies.
