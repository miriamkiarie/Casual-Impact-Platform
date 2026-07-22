# Casual-Impact-Platform
Built a complete causal impact platform that measures intervention effectiveness, identifies responsive customers, and deploys models through OCI MLOps pipelines.
An end-to-end experimentation, causal inference, uplift modeling, and MLOps framework designed to measure whether business interventions actually cause outcomes.

---

## Overview

Most analytics projects answer questions such as:

- Which customers are likely to churn?
- Which customers are likely to convert?
- Which products are likely to sell?

This project answers a different question:

> Did our intervention actually make a difference?

The Causal Impact Platform provides a complete workflow for designing experiments, measuring causal effects, identifying customers who genuinely respond to treatment, and deploying those insights into production.

The platform covers the full experimentation lifecycle:

1. Power Analysis & Experimental Design
2. Sequential A/B Testing
3. Quasi-Experimental Methods
4. Uplift Modeling
5. OCI MLOps Deployment

The project extends a customer churn prediction system. While the churn model predicts who is at risk of leaving, this platform evaluates whether retention actions actually influence customer behavior.

---

## Business Problem

Organizations spend significant resources on:

- Marketing campaigns
- Customer retention initiatives
- Pricing changes
- Product launches
- Operational improvements

Yet many teams struggle to answer:

- Did the intervention cause the outcome?
- Was the result statistically significant?
- Which customers actually benefited?
- Was the campaign worth the investment?

This platform was built to answer those questions using rigorous experimentation and causal inference techniques.

---

## Solution Architecture

```text
Business Problem
       │
       ▼
Power Analysis & Experiment Design
       │
       ▼
Sequential A/B Testing
       │
       ▼
Causal Impact Estimation
       │
       ▼
Uplift Modeling
       │
       ▼
OCI MLOps Deployment
       │
       ▼
Monitoring & Drift Detection
       │
       ▼
New Data & Outcomes
       │
       ▼
Improved Future Experiments
```

The architecture creates a continuous learning cycle where experiment outcomes generate evidence that improves future business decisions.

---

# Project Structure

```text
project4-causal-impact-platform/
│
├── notebooks/
│   ├── 01_power_analysis.ipynb
│   ├── 02_ab_test_engine.ipynb
│   ├── 03_quasi_experimental_methods.ipynb
│   ├── 04_uplift_modeling.ipynb
│   └── 05_oci_mlops.ipynb
│
├── src/
│   ├── experiment_designer.py
│   ├── ab_test_engine.py
│   ├── quasi_experimental.py
│   ├── uplift_modeling.py
│   └── mlops_pipeline.py
│
├── tests/
│
├── models/
│
├── reports/
│
├── deployment/
│
└── README.md
```

---

# Notebook 1: Power Analysis & Experimental Design

## Objective

Determine whether an experiment is worth running and calculate the required sample size before launch.

### Features

- Sample size calculation
- Statistical power analysis
- Sequential testing simulations
- O'Brien-Fleming boundaries
- Pocock boundaries
- Bayesian power estimation
- E-value sensitivity analysis
- Cost-benefit optimization
- Attrition-aware planning

### Validation

Statistical calculations were validated using:

- Statsmodels
- Monte Carlo simulations

---

# Notebook 2: Sequential A/B Testing Engine

## Objective

Monitor experiments throughout their lifecycle while controlling false positive rates.

### Features

- Sequential monitoring
- Interim analysis
- Conditional power calculations
- Early stopping for efficacy
- Early stopping for futility
- O'Brien-Fleming boundaries
- Pocock boundaries

### Output Decisions

- Continue Experiment
- Stop for Efficacy
- Stop for Futility

---

# Notebook 3: Quasi-Experimental Methods

## Objective

Estimate causal effects when randomized experiments are not available.

### Methods

#### Difference-in-Differences (DiD)

Used when treatment and control groups exist but randomization is unavailable.

Key assumption:

- Parallel Trends

#### Propensity Score Matching (PSM)

Used to reduce selection bias in observational data.

Capabilities:

- Covariate balancing
- Treatment effect estimation
- Matching diagnostics
- Bias reduction measurement

### Applications

- Marketing campaigns
- Product launches
- Historical intervention analysis
- Policy evaluation

---

# Notebook 4: Uplift Modeling

## Objective

Identify customers who genuinely benefit from treatment.

Traditional models answer:

> Who is likely to churn?

Uplift models answer:

> Who changes behavior because of treatment?

### Implemented Methods

#### T-Learner

- Treatment model
- Control model
- Individual treatment effect estimation

#### Class Transformation

- Single-model uplift learning
- Propensity-adjusted estimation

### Evaluation Metrics

- Qini Curve
- Qini Coefficient
- AUUC

### Customer Segments

- Persuadables
- Sure Things
- Lost Causes
- Sleeping Dogs

These segments allow organizations to allocate intervention budgets more effectively.

---

# Notebook 5: OCI MLOps Deployment

## Objective

Deploy experimentation workflows into a governed production environment.

### Pipeline Components

#### Data Validation

- Schema checks
- Missing value checks
- Treatment balance validation

#### Feature Engineering

Automated and reproducible feature generation.

#### Model Training

- Deterministic training
- Reproducible workflows
- Version-controlled artifacts

#### Quality Gates

Deployment is blocked if model quality thresholds are not met.

#### Model Registry

OCI Model Catalog integration:

- Model versioning
- Artifact tracking
- Auditability
- Reproducibility

#### Deployment

Real-time inference endpoint creation.

#### Monitoring

- Population Stability Index (PSI)
- Data drift monitoring
- Performance degradation detection

---

# Continuous Learning Framework

The platform supports evidence-based decision making through a continuous feedback loop.

```text
Experiment Design
        │
        ▼
Run Experiment
        │
        ▼
Measure Impact
        │
        ▼
Identify Responders
        │
        ▼
Deploy Insights
        │
        ▼
Monitor Outcomes
        │
        ▼
Collect New Data
        │
        ▼
Improve Future Experiments
```

As more experiments are conducted, the organization develops a stronger understanding of which interventions generate measurable business value.

---

# Testing & Reliability

The project includes a comprehensive automated testing suite covering:

- Statistical calculations
- Sequential testing logic
- Quasi-experimental methods
- Uplift modeling
- Input validation
- Edge cases
- Regression testing

## Test Coverage

| Module | Purpose |
|----------|----------|
| Experimental Design | Sample size, power analysis |
| A/B Testing Engine | Sequential testing logic |
| Quasi Experimental | DiD and PSM validation |
| Uplift Modeling | Uplift estimation and segmentation |
| MLOps Pipeline | Deployment workflow validation |

---

# Technology Stack

## Data Science

- Python
- NumPy
- Pandas
- SciPy
- Statsmodels
- Scikit-Learn

## Experimentation

- A/B Testing
- Sequential Analysis
- Bayesian Statistics
- Causal Inference

## Machine Learning

- Gradient Boosting
- Uplift Modeling
- Probability Calibration

## MLOps

- Oracle Cloud Infrastructure (OCI)
- OCI Data Science
- OCI Model Catalog
- OCI DevOps
- Terraform
- GitHub Actions

---

# Skills Demonstrated

- Experimental Design
- Statistical Inference
- Causal Analysis
- Uplift Modeling
- Machine Learning
- Software Engineering
- Automated Testing
- MLOps
- Cloud Deployment
- Model Monitoring

---

# Future Enhancements

- Automated retraining workflows
- Champion-Challenger models
- Multi-Armed Bandits
- Causal Forests
- Real-time uplift APIs
- Automated intervention recommendations

---

# Author

**Miriam Kiarie**



