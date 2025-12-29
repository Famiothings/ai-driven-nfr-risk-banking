# ai-driven-nfr-risk-banking
AI-Driven Non-Financial Risk Prediction and Control Effectiveness System for Banking. 

Capstone Project – Post Graduate Diploma in Artificial Intelligence and Machine Learning (Dec 2024). 

School: Asian Institute of Management (AIM) – Emeritus

---

# Note to the Evaluator: 
All detailed steps for preprocessing, EDA, visual representations (distributions,correlation matrix, tables, pair plots, etc.), model creation and training are documented with reproducible code and can be found in 'AI_Driven_NFR_Prediction_for_Banking.ipynb'. The whole notebook is designed and coded to be fully executable in Google Colab.

---

# AI-Driven Non-Financial Risk Prediction and Control Effectiveness System for Banking

## Project Overview
This capstone project develops an AI-driven decision support system for **Non-Financial Risk (NFR) management in a banking context**. The solution applies supervised machine learning to predict the likelihood of a non-financial risk event occurring within the next 30 days and to estimate the potential financial severity of such events. Emphasis is placed on explainability, governance, and business-aligned risk prioritisation.

The project is designed to reflect real-world banking constraints, including rare-event prediction, limited investigation capacity, and regulatory expectations for model transparency.

---

## Objectives
- Predict non-financial risk event occurrence within the next 30 days (classification)
- Estimate financial severity conditional on event occurrence (regression)
- Prioritise business units based on predicted risk
- Provide explainable and auditable model outputs using SHAP
- Align technical modeling with non-financial risk governance requirements

---

## Dataset
- **Records:** 10,000 (synthetic)
- **Business Units:** 120
- **Time Span:** 2 years
- **Key Feature Groups:**
  - Key Risk Indicators (KRIs)
  - Risk and Control Self-Assessment (RCSA) measures
  - HR metrics (attrition, tenure)
  - IT change indicators
  - External risk signals
  - Incident narratives
- **Target Variables:**
  - `target_event_30d` (binary classification)
  - `target_severity_amt` (regression)

> Note: The dataset is synthetic and used strictly for academic purposes.

---

## Methodology
1. **Data Preparation**
   - Data preprocessing, conversion, duplicate handling, missing values handling
   - Outliers handling

2. **Exploratory Data Analysis**
   - Correlation assessment
   - Distributional analysis
   - Class imbalance identification
   - PCA for structural insight (not used in final modeling)

3. **Feature Engineering**
   - Domain-driven interaction features
   - Tail-risk indicators
   - Risk escalation metrics

4. **Modeling**
   - Supervised learning framework
   - Classification and Regression modeled separately
   - Models evaluated (Classification): Logistic Regression, Decision Tree, Random Forest, SVM, LightGBM
   - Models evaluated (Regerssion): Logistic Regression, Decision Tree, Random Forest, LightGBM

5. **Evaluation**
   - Classification: Recall, PR-AUC, Recall@Top-10%
   - Regression: MAE, RMSE
   - Threshold tuning for business-aligned decision making
   - LightGBM selected as final model for both tasks
  
6. **Experimentation on Other Models**
   - Unsupervised Models: K-Means, DBSCAN, Hierarchical (Elbow and Silhoutte)
   - Recommender System
   - Deep Learning (not applicable, for further study)

7. **Explainability & Governance**
   - SHAP for local and global explanations
   - Addressed Limitations: Class Imbalance, Target Leakage, Overfitting
   - Bias and fairness considerations

8. **Solving the Business Problem**
   - Event Occurrence: Identified business units that will most-likely experience a NFR event in the next 30 days
   - Severity Amount: Predicted potential financial loss that could be avoided
  
9. **Future Recommendations and Areas for Further Study**
   - Dynamic, adaptive risk thresholds
   - Monitoring and refining features and evaluation metrics 
   - More unstructured data (incident narratives, audit findings, regulatory messages) 


---

## Repository Structure

ai-driven-nfr-risk-banking/
  - data/: contains the 1 file of synthethic NFR data used for this project
  - models/: contains 15 models (structured, unstructured, recommender, preprocessing)
  - notebooks/: contains 1 full notebook and README as note to the evaluator
  - presentation/: contains 4 files for business and technical decks
  - report/: contains the final capstone project report
  - requirements.txt: contains the requirements 


