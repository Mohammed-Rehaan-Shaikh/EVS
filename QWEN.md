# QWEN.md

## HCL GUVI × JAIN UNIVERSITY --- DataOps & MLOps Capstone

### Purpose

This repository is for the **HCL GUVI × JAIN University DataOps & MLOps
Capstone Project**.

The objective is to build a **working, explainable, end-to-end DataOps +
MLOps solution** for the project assigned to the group.

Every student must make a real technical contribution and be able to
explain: - Their own implementation. - The overall project workflow. -
The technical decisions made in the project. - The results produced by
the system.

The capstone should prioritize **implementation, integration, results,
reproducibility, and technical understanding**, not only presentation.

------------------------------------------------------------------------

## 1. Source of Requirements

The authoritative project requirements come from:

**HCL GUVI × JAIN UNIVERSITY --- DATAOPS & MLOPS CAPSTONE PROJECT ---
Student Guide**

The guide describes: - The capstone objective. - The practical
environment. - The common end-to-end architecture. - Group project
topics. - Student responsibilities. - Minimum technical requirements. -
One-week development plan. - Final presentation requirements. -
Evaluation criteria. - Technical questions students should be prepared
to answer. - Final submission checklist. - Team rules and important
dates.

Do not claim an implementation as complete unless it actually exists and
can be demonstrated.

------------------------------------------------------------------------

## 2. Core Project Objective

Build an end-to-end machine-learning system covering the relevant stages
from data to prediction and operational monitoring.

The expected workflow is:

``` text
DATA SOURCE
    ↓
DATA INGESTION
    ↓
DATA VALIDATION / QUALITY
    ↓
TRANSFORMATION / FEATURE ENGINEERING
    ↓
MODEL TRAINING
    ↓
MLFLOW EXPERIMENT TRACKING
    ↓
MODEL VALIDATION
    ↓
INFERENCE / DEPLOYMENT
    ↓
MONITORING
```

Apache Airflow should orchestrate relevant workflow steps.

Git/GitHub should be used for version control and reproducibility.

Prometheus and Grafana should be used for appropriate
operational/application monitoring.

------------------------------------------------------------------------

## 3. Practical Environment

The capstone guide specifies the following environment:

  -----------------------------------------------------------------------
  Component               Purpose                 Minimum Evidence
  ----------------------- ----------------------- -----------------------
  Jupyter                 Data analysis,          Working notebooks/code
                          preprocessing, feature  
                          engineering and ML      

  Apache Airflow          Workflow orchestration  DAG + successful run
                          and scheduling          

  MLflow                  Experiment tracking and Run, parameters,
                          model/artifact          metrics and
                          management              model/artifact evidence

  Docker                  Containerized           Relevant container
                          environment / packaging evidence
                          where required          

  Prometheus              Metrics collection      Relevant
                                                  project/application
                                                  metrics

  Grafana                 Monitoring              Meaningful
                          visualization           dashboard/panels

  Git/GitHub              Version control and     Repository with
                          reproducibility         meaningful commits
  -----------------------------------------------------------------------

### Important environment rule

Use only the URL and credentials assigned to the group.

Do not share group credentials with other groups.

------------------------------------------------------------------------

## 4. Possible Group Projects

The student guide defines 12 group scenarios:

1.  Customer Churn Prediction --- Classification + DataOps + MLOps
2.  Credit Card Fraud Detection --- Classification + monitoring
3.  E-Commerce Sales Prediction --- Regression / forecasting + pipeline
4.  Loan Default Prediction --- Classification + MLflow
5.  Telecom Customer Retention --- Classification + workflow
6.  Insurance Claim Prediction --- Classification + pipeline
7.  Retail Demand Forecasting --- Forecasting + DataOps
8.  Employee Attrition Prediction --- Classification + MLOps
9.  Delivery Time Prediction --- Regression + inference
10. Manufacturing Quality Prediction --- Classification + monitoring
11. Food Delivery Order Cancellation Prediction --- Classification +
    workflow + monitoring
12. Student Exam Performance Prediction --- Classification + DataOps +
    MLOps

The assigned project must not be changed without trainer approval.

------------------------------------------------------------------------

## 5. Five Student Responsibility Areas

Each student should have an identifiable technical contribution.

### Responsibility 1 --- Data Ingestion

Expected work: - Obtain the project dataset. - Implement ingestion. -
Handle the source appropriately. - Handle files, APIs, or databases as
applicable.

The student should be able to explain: - Where the data came from. - How
it is ingested. - What ingestion method is used. - How
files/API/database inputs are handled.

### Responsibility 2 --- Data Quality + Transformation

Expected work: - Data validation. - Data cleaning. - Data
transformation. - Feature engineering.

The student should be able to explain: - What quality problems were
identified. - How those problems were handled. - Which transformations
were applied. - Which features were created. - Why the selected
transformations/features are relevant.

### Responsibility 3 --- ML + MLflow

Expected work: - Select and train an appropriate ML model. - Evaluate
the model. - Track experiments using MLflow. - Store relevant artifacts.

The student should be able to explain: - Why the model was selected. -
Which parameters were used. - Which metrics were measured. - What the
metrics mean. - How the experiment was tracked in MLflow. - What
model/artifacts were stored.

### Responsibility 4 --- Airflow + Inference/Deployment

Expected work: - Create the Airflow DAG. - Define workflow tasks and
dependencies. - Run the workflow successfully. - Implement the
prediction/inference path. - Implement deployment/API components where
appropriate.

The student should be able to explain: - What each DAG task does. - Task
dependencies. - What happens if an Airflow task fails. - How data moves
through the prediction path. - How an input reaches the model and
produces a prediction.

### Responsibility 5 --- Monitoring + Integration + Documentation

Expected work: - Integrate the components. - Collect relevant metrics. -
Build Prometheus/Grafana monitoring. - Document the project in the
README.

The student should be able to explain: - What metrics are monitored. -
What the Grafana dashboard shows. - How the components are integrated. -
How the end-to-end workflow operates.

------------------------------------------------------------------------

## 6. Mandatory Technical Requirements

The final project should include evidence for all applicable
requirements:

-   [ ] Problem statement.
-   [ ] Business objective.
-   [ ] ML target.
-   [ ] Dataset description.
-   [ ] Important features.
-   [ ] Data ingestion implementation.
-   [ ] Data-quality / validation implementation.
-   [ ] Data transformation.
-   [ ] Feature engineering.
-   [ ] At least one appropriate ML model.
-   [ ] Suitable model metrics.
-   [ ] MLflow experiment tracking.
-   [ ] MLflow parameters.
-   [ ] MLflow metrics.
-   [ ] MLflow model/artifact evidence.
-   [ ] Airflow DAG.
-   [ ] At least one successful Airflow execution.
-   [ ] Working inference/prediction path.
-   [ ] API/deployment where appropriate.
-   [ ] Prometheus/Grafana or relevant operational monitoring evidence.
-   [ ] Git/GitHub repository.
-   [ ] Meaningful Git commits.
-   [ ] README containing setup, architecture, execution steps and
    results.
-   [ ] Final PPT.
-   [ ] Individual contribution sheet.

------------------------------------------------------------------------

## 7. Recommended Repository Structure

Adapt this structure to the assigned project rather than creating
unnecessary files:

``` text
project-root/
│
├── README.md
├── QWEN.md
├── requirements.txt
├── .gitignore
├── docker-compose.yml
├── Dockerfile
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── features/
│
├── notebooks/
│   ├── data_analysis.ipynb
│   ├── preprocessing.ipynb
│   └── model_training.ipynb
│
├── src/
│   ├── ingestion/
│   ├── validation/
│   ├── transformation/
│   ├── features/
│   ├── training/
│   └── inference/
│
├── airflow/
│   └── dags/
│       └── project_pipeline.py
│
├── mlflow/
│   └── ...
│
├── api/
│   └── ...
│
├── monitoring/
│   ├── prometheus/
│   └── grafana/
│
├── models/
│   └── ...
│
├── tests/
│   └── ...
│
└── docs/
    ├── architecture/
    ├── presentation/
    └── contribution/
```

Only create directories that are actually needed by the implementation.

------------------------------------------------------------------------

## 8. One-Week Development Plan

Follow the capstone guide's intended sequence.

### Day 1 --- Problem + Architecture

Complete: - Problem definition. - Business objective. - ML target. -
Dataset selection. - Initial feature understanding. - System
architecture. - Team roles.

Expected output:

``` text
Problem definition
Architecture
Roles
```

### Day 2 --- Data Ingestion + Data Quality

Complete: - Data ingestion. - Data validation. - Missing-value checks. -
Duplicate checks. - Data-type checks. - Range/consistency checks where
relevant. - Initial cleaning.

Expected output:

``` text
Ingestion code
Validation checks
Cleaned data
```

### Day 3 --- Transformation + Feature Engineering

Complete: - Data transformation. - Encoding where required. - Scaling
where required. - Feature creation. - Feature selection where
appropriate.

Expected output:

``` text
Prepared dataset/features
```

### Day 4 --- Model Training + MLflow

Complete: - Train an appropriate model. - Evaluate the model. - Record
parameters. - Record metrics. - Save model/artifacts. - Track the
experiment in MLflow.

Expected output:

``` text
Trained model
Metrics
MLflow run
Model/artifact evidence
```

### Day 5 --- Airflow + Inference/Deployment

Complete: - Create the Airflow DAG. - Define task dependencies. -
Execute the DAG successfully. - Connect the relevant pipeline stages. -
Implement the prediction/inference path. - Add API/deployment if
appropriate.

Expected output:

``` text
Airflow DAG
Successful DAG run
Prediction path
```

### Day 6 --- Monitoring + End-to-End Integration

Complete: - Integrate the pipeline. - Expose relevant
application/project metrics. - Configure Prometheus. - Create meaningful
Grafana panels. - Verify the complete workflow.

Expected output:

``` text
Monitoring evidence
Integrated workflow
```

### Day 7 --- Testing + Documentation + Presentation

Complete: - Test the complete project. - Fix remaining issues. - Update
README. - Prepare architecture diagram. - Prepare final PPT. - Prepare
individual contribution sheet. - Practice technical Q&A. - Verify that
every claimed feature can be demonstrated.

Expected output:

``` text
Final repository
Documentation
PPT
Contribution sheet
Working demo
```

------------------------------------------------------------------------

## 9. DataOps Guidelines

The DataOps portion should clearly show how data moves through the
system.

### Data ingestion

Document: - Data source. - Input format. - Ingestion method. -
Destination/storage. - Relevant error handling.

### Data validation

Where applicable, check: - Missing values. - Duplicate records. -
Invalid data types. - Unexpected categories. - Invalid ranges. -
Inconsistent values. - Target-label issues. - Other project-specific
quality problems.

Do not add arbitrary checks simply to increase complexity. Checks should
be relevant to the dataset and business problem.

### Transformation

Document: - Cleaning operations. - Encoding. - Scaling. - Aggregation. -
Feature creation. - Feature selection.

Every important transformation should have a clear reason.

------------------------------------------------------------------------

## 10. MLOps Guidelines

### Model training

Use at least one appropriate ML model.

Record: - Model type. - Training data. - Validation/test strategy. -
Hyperparameters. - Evaluation metrics. - Final model artifact.

### Metrics

Select metrics appropriate to the ML problem.

For classification, potentially relevant metrics include: - Accuracy. -
Precision. - Recall. - F1-score. - ROC-AUC.

For regression, potentially relevant metrics include: - MAE. - MSE. -
RMSE. - R².

For forecasting, use metrics appropriate to the forecasting setup.

Do not select metrics without understanding what they measure.

### MLflow

The MLflow implementation should provide evidence of: -
Experiment/run. - Parameters. - Metrics. - Model/artifacts.

The README should explain how to reproduce or inspect the MLflow run.

------------------------------------------------------------------------

## 11. Airflow Guidelines

The Airflow DAG should represent the actual project workflow.

A typical dependency structure may look like:

``` text
ingest
  ↓
validate
  ↓
transform
  ↓
feature_engineering
  ↓
train
  ↓
evaluate
  ↓
register/save_model
  ↓
inference
```

The exact DAG should be adapted to the assigned project.

Be prepared to explain: - Every task. - Task order. - Dependencies. -
Inputs and outputs. - Failure behavior. - How the DAG was executed
successfully.

Do not create an Airflow DAG that is disconnected from the actual
implementation merely for demonstration.

------------------------------------------------------------------------

## 12. Inference / Prediction Path

The final project must have a working path from input to prediction.

Conceptually:

``` text
User / Application Input
        ↓
Input Validation
        ↓
Preprocessing / Feature Transformation
        ↓
Trained Model
        ↓
Prediction
        ↓
Response / Result
```

If an API is used, document: - Endpoint. - Input format. - Validation. -
Model loading. - Prediction logic. - Output format. - Error handling.

The prediction path must use the actual trained model and compatible
preprocessing.

------------------------------------------------------------------------

## 13. Monitoring

Prometheus and Grafana should provide meaningful operational/application
monitoring.

Potential metrics may include: - Request count. - Prediction count. -
Prediction latency. - Error count. - Application health. - Pipeline
execution status. - Other metrics relevant to the project.

Grafana should contain meaningful panels rather than screenshots or
decorative charts.

Be able to explain: - What each metric represents. - Why it is being
monitored. - Where the metric comes from. - What the dashboard
indicates.

------------------------------------------------------------------------

## 14. Docker

Use Docker where required by the project/environment.

Containerization should help provide a reproducible environment for
relevant services.

If Docker Compose is used, clearly identify the services and their
relationships.

Do not add containers that are unnecessary for the actual project.

------------------------------------------------------------------------

## 15. Git/GitHub Rules

Use Git/GitHub throughout development.

Commits should be meaningful and reflect actual progress.

Prefer commits such as:

``` text
feat: add data ingestion pipeline
feat: add data validation checks
feat: add feature engineering
feat: train baseline model
feat: integrate MLflow tracking
feat: add Airflow DAG
feat: add inference API
feat: add Prometheus metrics
feat: add Grafana dashboard
docs: update README
fix: resolve inference preprocessing issue
```

Avoid using a single final commit for the entire project.

Do not commit: - Credentials. - Passwords. - API keys. - Private URLs
when inappropriate. - Large unnecessary datasets. - Local environment
files containing secrets.

Use `.gitignore` appropriately.

------------------------------------------------------------------------

## 16. README Requirements

The README should contain at minimum:

### Project Overview

-   Project title.
-   Problem statement.
-   Business objective.
-   ML target.

### Dataset

-   Dataset source.
-   Dataset description.
-   Important features.
-   Target variable.

### Architecture

-   End-to-end architecture diagram.
-   Explanation of each major component.

### DataOps

-   Ingestion.
-   Validation.
-   Transformation.
-   Feature engineering.

### MLOps

-   Model.
-   Training.
-   Metrics.
-   MLflow.

### Airflow

-   DAG description.
-   Tasks.
-   Dependencies.
-   Execution instructions.

### Inference

-   Prediction workflow.
-   API/deployment instructions where applicable.

### Monitoring

-   Prometheus.
-   Grafana.
-   Important metrics/panels.

### Setup

-   Requirements.
-   Environment setup.
-   Docker commands if applicable.
-   Service startup instructions.

### Execution

-   How to run the pipeline.
-   How to train the model.
-   How to run inference.
-   How to access monitoring.

### Results

-   Actual model metrics.
-   Relevant screenshots/evidence.
-   Important observations.

### Reproducibility

-   Git repository.
-   Configuration.
-   Required dependencies.
-   Execution sequence.

------------------------------------------------------------------------

## 17. Final Presentation

Maximum duration: **10 minutes**.

Recommended structure from the guide:

  -----------------------------------------------------------------------
  Time                                Content
  ----------------------------------- -----------------------------------
  1 min                               Business problem + ML objective

  2 min                               Architecture + end-to-end flow

  2 min                               DataOps: ingestion, quality,
                                      transformation and Airflow

  2 min                               MLOps: model, metrics, MLflow and
                                      inference

  1 min                               Monitoring: Prometheus/Grafana or
                                      relevant monitoring evidence

  2 min                               Results + individual
                                      contributions + questions
  -----------------------------------------------------------------------

All 5 students must participate.

The trainer may ask any student to: - Open code. - Explain their
contribution. - Explain the project workflow. - Answer technical
questions.

Demonstrate actual implementation, not only PPT screenshots.

------------------------------------------------------------------------

## 18. Evaluation Criteria

The capstone is evaluated out of 100 marks:

  Evaluation Area                          Marks
  ------------------------------------ ---------
  Business problem & objective                10
  Architecture & design                       10
  DataOps implementation                      15
  MLOps implementation                        15
  End-to-end integration                      10
  Git/GitHub & reproducibility                 5
  Documentation / README                       5
  Final demo / presentation                   10
  Individual contribution                     10
  Individual technical understanding          10
  **Total**                              **100**

The implementation should therefore be built with both **technical
completeness** and **individual explainability** in mind.

------------------------------------------------------------------------

## 19. Technical Questions to Prepare For

Every team member should be able to answer:

1.  Why did your group choose this problem and target?
2.  Where did the dataset come from?
3.  What data-quality issues did you identify?
4.  How did you handle those issues?
5.  What transformations did you perform?
6.  What features did you create?
7.  Why did you create those features?
8.  Which model did you use?
9.  Why did you use that model?
10. Which metrics did you use?
11. What do those metrics mean?
12. How did you track the experiment in MLflow?
13. What does your Airflow DAG do?
14. What are the Airflow tasks and dependencies?
15. What happens if an Airflow task fails?
16. How does the prediction/inference path work?
17. What does the monitoring dashboard show?
18. What code did you personally implement?
19. What technical problem did you face?
20. How did you solve it?

Answers should be based on the actual implementation in the repository.

------------------------------------------------------------------------

## 20. Final Submission Checklist

Before final evaluation, verify:

``` text
[ ] Problem statement
[ ] Business objective
[ ] ML target
[ ] Dataset description
[ ] Important features
[ ] Architecture diagram
[ ] Data ingestion
[ ] Data-quality / validation
[ ] Transformation
[ ] Feature engineering
[ ] Model
[ ] Actual model results and metrics
[ ] MLflow run
[ ] MLflow parameters
[ ] MLflow metrics
[ ] MLflow model/artifact evidence
[ ] Airflow DAG
[ ] Successful Airflow execution
[ ] Inference / prediction path
[ ] Prometheus/Grafana monitoring evidence
[ ] GitHub repository
[ ] Meaningful Git commits
[ ] README
[ ] Final PPT
[ ] Individual contribution sheet
[ ] All team members prepared for technical Q&A
```

------------------------------------------------------------------------

## 21. Team Rules

1.  Do not change the assigned project without trainer approval.
2.  Do not share the group's Jupyter URL or credentials with other
    groups.
3.  Keep code, notebooks, configuration and documentation organized in
    Git/GitHub.
4.  Do not claim a feature or implementation that cannot be
    demonstrated.
5.  Each student must understand their own contribution and the overall
    project flow.
6.  Use the provided practical environment responsibly.
7.  Avoid changing shared infrastructure unnecessarily.
8.  Be ready to demonstrate the working project, not only the PPT.

------------------------------------------------------------------------

## 22. Important Dates

According to the capstone guide:

  -----------------------------------------------------------------------
  Activity                            Date / Time
  ----------------------------------- -----------------------------------
  Capstone Kickoff                    17 September 2026

  Progress / Mentoring Check          Saturday, 26 September 2026 ---
                                      9:00 AM to 10:00 AM

  Final Submission & Presentation     Thursday, 1 October 2026 --- 2
                                      hours
  -----------------------------------------------------------------------

The final evaluation includes: - Working project demonstration. -
Presentation. - Evaluation. - Technical Q&A.

------------------------------------------------------------------------

## 23. Instructions for Qwen / AI Coding Assistance

When working on this repository:

### Understand before modifying

Before making changes: 1. Inspect the existing repository structure. 2.
Identify the current implementation. 3. Read relevant configuration
files. 4. Understand the data flow. 5. Check existing dependencies. 6.
Avoid replacing working components unnecessarily.

### Preserve the project architecture

Do not introduce unnecessary technologies or services.

Prefer the technologies specified by the capstone environment: -
Python - Jupyter - Apache Airflow - MLflow - Docker - Prometheus -
Grafana - Git/GitHub

Use additional technologies only when they serve a clear project
requirement.

### Do not fabricate evidence

Never invent: - Model metrics. - MLflow runs. - Airflow execution
results. - Monitoring values. - Dataset statistics. - Successful
deployment results. - Screenshots. - Test results.

If something has not been executed or verified, state that it needs to
be tested.

### Keep implementations explainable

Prefer clear, beginner-friendly code over unnecessary abstraction.

Important logic should be easy for a student to explain during the final
Q&A.

### Preserve reproducibility

When changing the project: - Update requirements when dependencies
change. - Keep configuration documented. - Keep paths portable where
possible. - Avoid hard-coded personal machine paths. - Keep secrets
outside source control. - Update README instructions when execution
changes.

### Test changes

After modifying code: 1. Check syntax. 2. Run the relevant component
where possible. 3. Verify outputs. 4. Check integration with dependent
components. 5. Report any untested portion clearly.

### Keep student ownership visible

When implementing a feature, make it possible for the student to
explain: - What was changed. - Why it was changed. - How it works. - How
it was tested. - What output it produces.

------------------------------------------------------------------------

## 24. Working Principle

The goal is not to build a large or unnecessarily complicated system.

The goal is to build a **working, reproducible, explainable end-to-end
DataOps + MLOps project** that satisfies the capstone requirements and
can be demonstrated during the final evaluation.

When choosing between two valid implementations, prefer the one that is:

1.  Correct.
2.  Demonstrable.
3.  Reproducible.
4.  Explainable.
5.  Consistent with the provided capstone environment.
6.  Appropriate for the assigned problem.

------------------------------------------------------------------------

## 25. Primary Reference

**HCL GUVI × JAIN UNIVERSITY\
DATAOPS & MLOPS CAPSTONE PROJECT\
Student Guide • 12 Groups • One-Week Project Development & Final
Evaluation**

This `QWEN.md` is derived from the provided student guide and is
intended to give Qwen repository-level context while assisting with
implementation.
