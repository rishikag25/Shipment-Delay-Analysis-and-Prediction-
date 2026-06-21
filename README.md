# Supply Chain Bottleneck Analytics & Delay Prediction

An end-to-end data analytics and predictive modeling pipeline engineered to map logistics bottlenecks and forecast delivery delays across multi-merchant portfolios. This framework addresses data leakage and distribution instabilities inherent to disjoint transactional tracking databases.


##  Pipeline Architecture

* **Data Aggregation:** Ingestion of transaction histories spanning an 11,000-shipment multi-merchant portfolio.
* **Metric Engineering:** Development of custom analytical metrics, including Value Density and Customer Friction Indices.
* **Data-Leakage Prevention:** Cross-sectional splitting and partitioning across disjoint databases to stabilize distributions.
* **Hyperparameter Optimization:** Deployment of 3-fold cross-validated Grid Search CV to isolate optimal model states.
* **Predictive Modeling:** Application of regularized Lasso Regression and Random Forest ensembles.
* **Performance Validation:** Evaluation of temporal classification strength using peak ROC-AUC validation metrics.


##  Project Overview

Logistics networks frequently suffer from significant operational delays caused by systemic infrastructure bottlenecks and erratic merchant distribution patterns. This project delivers an automated analytics pipeline that uncovers hidden supply chain frictions and accurately predicts shipment disruptions before they impact customer satisfaction.


##  Data & Feature Engineering

### 1. Dataset Description
* **Data Scale:** Compiled historical shipping records encompassing **11,000 distinct merchant shipments**.
* **Structural Domain:** Encompasses transaction timestamps, carrier performance levels, regional tracking identifiers, and cost metrics.

### 2. Preprocessing & Metric Innovation
* **Custom Metrics:** Designed and computed the **Value Density Index** and **Customer Friction Index** to capture real-time shipment vulnerability.
* **Distribution Stabilization:** Implemented targeted distribution mapping across disparate data sources, isolating statistical anomalies without altering structural baseline traits.
* **Strict Leakage Prevention:** Built a data-leakage-free processing pipeline, ensuring target variables and post-delay indicators never contaminated the training partitions.


##  Methodology & Modeling Approach

### 1. Machine Learning & Predictive Refinement
* **Algorithms Deployed:** Implemented regularized **Lasso Regression** for continuous baseline optimization and **Random Forest** classification ensembles to capture non-linear disruption patterns.
* **Optimization Framework:** Executed a systematic **3-fold cross-validated Grid Search CV** routine to fine-tune tree depth, estimators, and regularization penalties.

### 2. Evaluation Strategy
* **Primary Metric:** Prioritized **ROC-AUC** to measure the true-positive classification trade-off across varying probability thresholds, ensuring the model remains robust against imbalanced delivery delay distributions.


##  Tech Stack & Tooling

* **Programming Language:** Python
* **Data Pipelines & Engineering:** NumPy, Pandas, Scikit-learn
* **Optimization & Validation:** Grid Search CV Modules
* **Visualization Engine:** Matplotlib, Seaborn


##  Data Source & Operational Signals

The analytical engine monitors core shipment parameters to isolate friction:
* **Target Objective:** Predicting binary delivery delays (On-Time vs. Delayed) and estimating exact arrival deviations.
* **Operational Inputs:** Merchant transit durations, carrier tier variables, geographic routing milestones, and cost-to-weight structural ratios.


##  Key Results & Deliverables

* **Leakage Erasure:** Maintained a zero-leakage framework across all validation checks.
* **Predictive Accuracy:** Achieved a peak validation **ROC-AUC of 0.741**, demonstrating strong practical reliability for predicting supply chain disruptions.
