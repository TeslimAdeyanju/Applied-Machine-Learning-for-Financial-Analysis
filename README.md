# Applied Machine Learning for Financial Analysis

> A structured portfolio of practical machine learning exercises covering regression, classification, risk modelling, model evaluation and deployment concepts, with financial and business applications.

**Status:** Seven numbered learning modules contain notebooks or code. Serverless and Kubernetes modules are proposed extensions, not implemented folders.

## Executive Summary

Financial analysis increasingly requires the ability to translate business questions into measurable prediction tasks, choose an appropriate baseline, evaluate uncertainty and communicate model limitations. This repository builds those capabilities through applied notebooks, comparative modelling exercises and a Flask deployment example.

The work follows the [DataTalks.Club Machine Learning Zoomcamp](https://github.com/DataTalksClub/machine-learning-zoomcamp), supplemented with independent exploration and finance-oriented interpretation. It is primarily a **learning and implementation portfolio**, not a single production finance application.

## Business and Learning Objectives

1. Frame prediction problems using business-oriented objectives and baseline metrics.
2. Prepare categorical and numerical data without training/test leakage.
3. Train and evaluate regression, classification and ensemble models.
4. Interpret error metrics and the costs of false positives and false negatives.
5. Package a fitted model behind an HTTP endpoint and explore deployment.
6. Apply these skills to customer churn, credit-related classification and price modelling.

## Learning Modules and Evidence

| Module | Repository content | Core competency |
| --- | --- | --- |
| [1. Introduction](1-introduction_to_machine-learning/) | Notebooks and sample datasets | Problem definition, initial exploration and CRISP-DM |
| [2. Regression](2-machine_learning_for_regression/) | Regression notebooks and data | Linear regression, transformations, regularisation and validation |
| [3. Classification](3-machine_learning_for_classification/) | Classification notebooks | Logistic regression, encoding, feature interpretation |
| [4. Evaluation](4-evaluation_metrics_for_classification/) | Evaluation notebook | Precision, recall, ROC AUC, validation and thresholds |
| [5. Deployment](5-machine_learning_deployment/) | Flask service, training code, test client, Dockerfile and saved model | Model packaging and HTTP inference |
| [6. Decision Trees and Ensembles](6-Decision_trees_and_ensemble_learning/) | Ensemble-learning notebook and data | Tree models, random forests and boosting |
| [7. Neural Networks](7-neural_networks_and_deep_learning/) | Deep learning notebook and images | Neural networks and image modelling |
| 8. Serverless deep learning | No implemented module directory | Future |
| 9. Kubernetes and model serving | No implemented module directory | Future |

**Scope note:** The datasets used in these exercises include general educational datasets. They are not all finance datasets, even where the methods can be applied to finance.

## Analytical Workflow

```mermaid
flowchart LR
 A[Business question and dataset] --> B[Exploration and preprocessing]
 B --> C[Baseline model]
 C --> D[Train and validate]
 D --> E[Error and risk assessment]
 E --> F[Model interpretation]
 F --> G[Deployment exercise where applicable]
```

## Selected Implementation: Churn Classification Service

The fifth module contains `train.py`, `predict.py`, `predict-test.py`, a saved model file and a Dockerfile. The Flask endpoint accepts JSON customer attributes and responds with a churn probability and a binary threshold result.

The inference script uses the model file `model_C=1.0.bin` relative to the working directory and exposes `POST /predict` on port 9696. This demonstrates a deployable design but is **not proof that a live service is currently hosted or monitored**.

```bash
cd 5-machine_learning_deployment
python -m pip install pipenv
pipenv install
pipenv run python predict.py
```

The command is a local development starting point, not a clean-environment execution guarantee. Run the test client only after the API is available, and inspect its configured URL.

## Reproducing the Learning Work

This repository mixes Jupyter notebooks and a deployment subproject with its own `Pipfile` and `Dockerfile`. Use the environment suitable for the selected module rather than assuming all notebooks share one runtime.

At the repository root, `pyproject.toml`, `uv.lock` and `.python-version` provide additional environment metadata.

```bash
git clone https://github.com/TeslimAdeyanju/Applied-Machine-Learning-for-Financial-Analysis.git
cd Applied-Machine-Learning-for-Financial-Analysis
uv sync
uv run jupyter lab
```

Check installed notebook dependencies before execution. Some examples require additional datasets or environment-specific setup.

## Evaluation and Model Boundaries

A model should be assessed against an appropriate baseline and a genuinely held-out dataset. Classification experiments should report precision, recall, F1, ROC AUC and threshold sensitivity where useful; regression tasks should report MAE or RMSE with appropriate units.

**Verified performance table:** Not included in this overview. Each module's own reproducible notebook outputs should be consulted before publishing numerical claims. The presence of a training script or serialized model does not establish accuracy, generalisation or production readiness.

## Repository Structure

```text
1-introduction_to_machine-learning/
2-machine_learning_for_regression/
3-machine_learning_for_classification/
4-evaluation_metrics_for_classification/
5-machine_learning_deployment/
6-Decision_trees_and_ensemble_learning/
7-neural_networks_and_deep_learning/
pyproject.toml
uv.lock
README.md
docs/
    readme-history.md
```

## Limitations and Next Steps

- Distinguish classroom examples from production-grade financial models.
- Publish a concise, reproducible evaluation table for each completed module.
- Confirm dependency compatibility and execution paths.
- Add automated tests for the Flask endpoint and validate deployment claims.
- Document training data provenance, leakage safeguards and model bias.
- Add serverless or Kubernetes modules only once implementation is present.

## Further Learning and References

[Detailed learning notes](https://adeyanjuteslim.notion.site/ML-02-Machine-Learning-Bookcamp-3e5807ec7963813b8660f2df94aa93d4) | [Machine Learning Zoomcamp](https://github.com/DataTalksClub/machine-learning-zoomcamp)

## Author

**Teslim Adeyanju**  
[Portfolio](https://adeyanjuteslim.co.uk) | [LinkedIn](https://www.linkedin.com/in/adeyanjuteslimuthman)

[Prior README](docs/readme-history.md)
