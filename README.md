# Applied Machine Learning for Financial Analysis

An applied machine learning portfolio built around real finance problems — price prediction, credit risk scoring, churn classification, and shipping the resulting models as deployed services. I built this on the structured foundation of DataTalks.Club's ML Zoomcamp, then took each project further: extra analysis, deeper write-ups, and a consistent financial-analysis framing across every module.

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-Gradient%20Boosting-016A70)](https://xgboost.readthedocs.io/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-FF6F00?logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![Flask](https://img.shields.io/badge/Flask-REST%20API-000000?logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![AWS](https://img.shields.io/badge/AWS-Elastic%20Beanstalk-FF9900?logo=amazonaws&logoColor=white)](https://aws.amazon.com/elasticbeanstalk/)

[![Notion](https://img.shields.io/badge/Notion-Full%20Write--ups-000000?logo=notion&logoColor=white)](https://adeyanjuteslim.notion.site/ML-02-Machine-Learning-Bookcamp-3e5807ec7963813b8660f2df94aa93d4)
Extended notes, extra experiments, and reflections behind every module in this repo.

---

## About This Project

Each module here tackles a finance-specific problem instead of a generic dataset: predicting asset and loan values, scoring credit risk, flagging customer churn, and packaging the resulting models as deployable services with Flask and Docker. The code, homework solutions, and datasets for each are in the numbered folders below; the reasoning, extra analysis, and lessons learned are written up on my [Notion page](https://adeyanjuteslim.notion.site/ML-02-Machine-Learning-Bookcamp-3e5807ec7963813b8660f2df94aa93d4).

I built the ML foundation for this through DataTalks.Club's [ML Zoomcamp](https://github.com/DataTalksClub/machine-learning-zoomcamp) (my working fork: [Fork8-machine-learning-zoomcamp](https://github.com/UthmanAdeyanju/Fork8-machine-learning-zoomcamp)), then expanded on it — the finance framing, the extra notebooks, and the deployment work are mine.

## Projects

| # | Module | What I Did |
|---|--------|------------|
| 1 | [Introduction to Machine Learning](1-introduction_to_machine-learning/) | Framed a real problem using the CRISP-DM methodology, distinguished supervised vs. rule-based approaches, and ran end-to-end EDA on a laptop pricing dataset to establish a baseline analysis workflow. |
| 2 | [Machine Learning for Regression](2-machine_learning_for_regression/) | Built an asset/price prediction model two ways — implementing linear regression from scratch with NumPy (normal equation) and again with scikit-learn — covering EDA, feature engineering, log-transforming skewed targets, L2 regularization, and RMSE-based validation. |
| 3 | [Machine Learning for Classification](3-machine_learning_for_classification/) | Built a customer churn/risk classifier with logistic regression, using `DictVectorizer` for categorical encoding, mutual information and correlation analysis for feature selection, and coefficient inspection to explain model decisions. |
| 4 | [Evaluation Metrics for Classification](4-evaluation_metrics_for_classification/) | Evaluated classifier performance beyond accuracy: precision/recall/F1, ROC curves and AUC, k-fold cross-validation, confusion matrices, and threshold tuning to handle class imbalance in the risk model. |
| 5 | [Machine Learning Deployment](5-machine_learning_deployment/) | Shipped the trained model as a production-style service — serialized with Pickle, served through a Flask REST API on Gunicorn, containerized with Docker, and configured for AWS Elastic Beanstalk deployment (`.ebextensions`), with a separate test client (`predict-test.py`) to verify the live endpoint. |
| 6 | [Decision Trees & Ensemble Learning](6-decision_trees_and_ensemble_learning/) | Built a credit-scoring model comparing decision trees, Random Forest, and XGBoost, with hyperparameter tuning (`max_depth`, `min_samples_leaf`, `n_estimators`, learning rate) and feature-importance ranking to explain what drives credit risk. |
| 7 | [Neural Networks & Deep Learning](7-neural_networks_and_deep_learning/) | Trained a CNN image classifier with TensorFlow/Keras, using transfer learning on a pretrained Xception model, data augmentation, and learning-rate tuning to improve generalization on a small image dataset. |
| 8 | Serverless Deep Learning | Deploying a deep learning model as a serverless endpoint with AWS Lambda and API Gateway. |
| 9 | Kubernetes & TensorFlow Serving | Serving and scaling ML models with Kubernetes and TensorFlow Serving. |

Each module folder contains a numbered lecture-note notebook, the homework solution, and any datasets specific to that module.

## Tech Stack

- **Modeling:** scikit-learn, XGBoost, TensorFlow/Keras
- **Data:** pandas, NumPy
- **Deployment:** Flask, Gunicorn, Docker, Pipenv, AWS Elastic Beanstalk
- **Language:** Python 3.8–3.10

## Connect

- **LinkedIn:** [www.linkedin.com/in/adeyanjuteslimuthman](https://www.linkedin.com/in/adeyanjuteslimuthman)
- **Portfolio:** [www.adeyanjuteslim.co.uk](https://www.adeyanjuteslim.co.uk)
- **Email:** info@adeyanjuteslim.co.uk

If you're working on something similar or want to collaborate — let's connect!
