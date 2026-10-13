# Churn Prediction — MLOps Labs 1–9

This repository combines the existing churn-prediction project (Labs 1–5 materials) with the numbered Lab 6–9 MLOps pipeline.

## Project areas
- `notebooks/project_implementation.ipynb` — notebook implementation and model experiments.
- `src/` — existing preprocessing, validation, training, and evaluation code.
- `pipelines/` — Lab 3–5 pipeline runners.
- `src/mlops_pipeline/` — Labs 6–9: data checks, preprocessing, MLflow model registry, evaluation, quality gate, lifecycle automation, inference, and failure-injection tests.
- `config.yaml` — settings for the Labs 6–9 pipeline.
- `.github/workflows/lab8_ci.yml` — GitHub Actions workflow for CI.
- `data/raw/churn.csv` — source dataset.

## Setup (run from the project root in VS Code terminal)

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Run the existing Lab 5 pipeline:

```bash
python pipelines/run_lab5_pipeline.py
```

Run the integrated Labs 6–9 pipeline:

```bash
python src/mlops_pipeline/churn_prediction_pipeline.py
```

Run Lab 9 failure-injection tests separately:

```bash
python src/mlops_pipeline/10_failure_injection.py
```

Run commands from the repository root so paths in `config.yaml` resolve correctly. The first run may create local MLflow tracking data, model files, reports, and outputs.

## GitHub update reminder
Changes made in VS Code are only local until you commit and push them. After checking the changes:

```bash
git status
git add .
git commit -m "Add MLOps Labs 6-9"
git push
```

Do not commit virtual environments or large generated files. Check `.gitignore` before pushing.
