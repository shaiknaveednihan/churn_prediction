# Labs 6–9 pipeline

The numbered scripts in this folder are the integrated Lab 6–9 workflow. Run `churn_prediction_pipeline.py` from the repository root, not from inside this folder. Configuration is in the root `config.yaml`.

Stages: load data → validate raw data → preprocess → validate outputs → train/register model → evaluate → quality gate → lifecycle promotion → inference. `10_failure_injection.py` contains Lab 9 failure tests and should be run separately.
