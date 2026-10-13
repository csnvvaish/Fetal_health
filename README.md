# CTG Assist — Fetal Health Classification

CTG Assist is a full-stack fetal health assessment support prototype built around machine learning and structured clinical assessment records.

The project aims to provide a clear interface for entering cardiotocography (CTG) measurements, obtaining a model-generated fetal health classification, and reviewing previous assessments.

**Important:** CTG Assist is an educational and research prototype, not a medical device or diagnostic system. Its predictions must not replace clinical judgment or professional medical assessment.

## Project Goals

- Develop and validate a reproducible fetal health classification pipeline.
- Build a REST API for validated inputs and model inference.
- Create a React frontend for assessment entry and results.
- Store assessment records and model-version information.
- Implement authentication and backend authorization.
- Evaluate model performance using class-wise metrics and leakage checks.
- Maintain reproducible documentation and version control.

## Planned Technology Stack

| Component | Technology |
|---|---|
| Frontend | React, Vite |
| Backend | Python, FastAPI, Pydantic |
| Machine learning | pandas, scikit-learn |
| Model persistence | joblib |
| Database | PostgreSQL |
| Database access and migrations | SQLAlchemy, Alembic |
| Testing | pytest |
| Version control | Git and GitHub |

These are planned technologies; implementation and compatibility will be verified during development.

## Planned Application Features

1. Secure clinician login and role-based access.
2. Validated CTG assessment input.
3. Model-generated classification with clearly explained limitations.
4. Assessment history and individual result details.
5. Model evaluation and version tracking.
6. Automated tests for input validation, authentication and prediction consistency.

## Machine Learning Validation

Before integrating the existing notebook, the project will verify:

- Dataset source, target definition and feature schema.
- Missing values, class distribution and preprocessing.
- Potential target leakage and duplicate or overlapping records.
- Appropriate stratified train/test evaluation.
- Macro F1-score, per-class recall and confusion matrix.
- Reproducible preprocessing and model inference.

Previously recorded notebook metrics will not be treated as verified until the experiments have been independently checked.

## Development Roadmap

- **Phase 1:** Audit the original notebook and document the ML pipeline.
- **Phase 2:** Validate the model and establish reproducible artifacts.
- **Phase 3:** Implement the FastAPI backend and database.
- **Phase 4:** Build and connect the React frontend.
- **Phase 5:** Add automated tests, security checks and deployment configuration.

## Data and Privacy

Use appropriately sourced, de-identified or synthetic development data. Do not enter real patient identifiers or sensitive clinical information into this prototype. Restrict access to stored records and protect authentication credentials.

## Project Status

The original machine-learning notebook has been committed to the `ctg-assist-development` branch. The dataset, model performance and application functionality remain subject to verification.

## Disclaimer

This project is intended for educational and research purposes only. It is not validated for clinical use and must not be used to make decisions about patient care.
