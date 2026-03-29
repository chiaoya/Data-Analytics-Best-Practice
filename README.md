# Data Analytics Best Practice

This project is a simple starter setup for running a data analysis notebook in VS Code.

## Files

- `data_case_study_template.ipynb`: general structured-data case study template for loading data, quality checks, cleaning, processing, EDA, and simple business insights
- `customer_segmentation_clustering_template.ipynb`: clustering template for customer segmentation with PCA-based 2D and 3D visualizations
- `supervised_modeling_template.ipynb`: regression, binary classification, and multiclass classification template with baseline models, random forest, XGBoost, and SHAP
- `experimentation_causal_inference_template.ipynb`: A/B testing, Difference-in-Differences, and propensity score weighting template
- `time_series_forecasting_template.ipynb`: forecasting template covering baseline, ARIMA, SARIMA, and optional LSTM/Transformer scaffolds
- `data.csv`: sample dataset so the notebook runs immediately
- `requirements.txt`: Python packages needed by the notebook

## Which Notebook To Use

- Use `data_case_study_template.ipynb` for most standard analytics case studies on structured tabular data
- Use `customer_segmentation_clustering_template.ipynb` when the task is unsupervised segmentation
- Use `supervised_modeling_template.ipynb` when the task is prediction or driver analysis
- Use `experimentation_causal_inference_template.ipynb` when the task is impact measurement or uplift
- Use `time_series_forecasting_template.ipynb` when the task is forecasting over time

## Run In VS Code

1. Open this folder in VS Code.
2. Open the terminal in VS Code.
3. Create a Python 3.11 virtual environment:

```bash
python3.11 -m venv .venv311
```

4. Activate it:

```bash
source .venv311/bin/activate
```

5. Install dependencies:

```bash
python -m pip install -r requirements.txt
```

6. Install the VS Code extensions:
   - Python
   - Jupyter

7. Open `data_case_study_template.ipynb`.
8. Click `Select Kernel` in the top right.
9. Choose the Python interpreter from `.venv311`.
10. Run the notebook cells from top to bottom.

Note: `tensorflow` and `torch` are included for optional sequence and transformer sections. If you want a lighter setup first, you can comment those lines out in `requirements.txt` and install them only when needed.

## Run A Single Cell

If you only want to run one cell at a time in VS Code:

1. Open `data_case_study_template.ipynb`.
2. Confirm the kernel is `.venv311`.
3. Hover over the cell you want to run.
4. Click the `Run` triangle on that cell.
5. To run the current cell with the keyboard, use:
   - `Shift+Enter`: run cell and move to the next one
   - `Ctrl+Enter` or `Cmd+Enter`: run the current cell and stay on it

This workspace includes a `.vscode/settings.json` file so the notebook cell toolbar stays visible and the project opens with the correct interpreter by default.

## Python Version Note

Use Python `3.11` for this project. Python `3.14` can cause notebook kernel issues in VS Code, including failing to run individual cells.

## Use Your Own Data

The notebook uses this line:

```python
DATA_PATH = Path('data.csv')
```

If you want to use another CSV:

- replace `data.csv` in the project root, or
- change `DATA_PATH` in the notebook

## Current Project Issues Found

- The original notebook depended on `data.csv`, but the file did not exist.
- The original notebook had a `pip install` cell inside the notebook, which is not a clean VS Code workflow.
- The original notebook included stale cell outputs and an import error for `matplotlib`.
- The original modeling example was not safe to run on common mixed-type datasets.

## Recommended Next Step

After the notebook runs successfully with the sample data, replace the sample CSV with your real dataset and update the markdown sections with your own business questions and findings.
