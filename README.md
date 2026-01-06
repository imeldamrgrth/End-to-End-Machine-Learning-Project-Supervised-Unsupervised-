# End-to-End Machine Learning Project (Supervised & Unsupervised)

## Overview
This project demonstrates a complete machine learning workflow combining **unsupervised** and **supervised** learning techniques. It focuses on clustering insurance customers and building classification models to predict cluster membership.  

The workflow covers:

1. Data preprocessing (scaling, encoding, cleaning)  
2. Unsupervised learning (K-Means clustering)  
3. Cluster analysis and interpretation  
4. Supervised learning (Random Forest, K-Nearest Neighbors)  
5. Model evaluation, hyperparameter tuning, and recommendations  

This project is suitable for showcasing an **end-to-end ML pipeline**, from raw data to actionable insights.

---

## Dataset
The dataset represents synthetic insurance claim data, including customer demographics and claim information. Key features include:

| Feature | Description |
|---------|-------------|
| `ClaimAmount` | Amount of insurance claim |
| `PatientAge` | Age of the customer/patient |
| `PatientIncome` | Annual income of the customer |
| `ProviderSpecialty` | Type of healthcare provider |
| `ClaimType` | Type of claim (Routine, Surgery, Emergency, Other) |
| `PatientEmploymentStatus` | Employment status of the customer |
| `ClaimSubmissionMethod` | How the claim was submitted (Online, Phone, Mail) |
| `Cluster` | Cluster label assigned by K-Means (target for supervised learning) |

**Data source:** Synthetic dataset created from clustering analysis.  

---

## Workflow

### 1. Data Preprocessing
- **Scaling:** Standardization of numeric features  
- **Encoding:** Label encoding for categorical features  
- **Train-test split:** 80% train, 20% test, stratified by cluster  

### 2. Unsupervised Learning
- Applied **K-Means clustering** to group customers into **Cluster 0 (Low Risk)** and **Cluster 1 (High Risk)**.  
- Evaluated cluster quality using **Silhouette Score** and **feature separation visualization**.  

### 3. Cluster Analysis
- Calculated **mean and mode** of features per cluster to interpret patterns:  
  - Cluster 0: Lower claim amounts, lower income, mostly routine claims via Mail.  
  - Cluster 1: Higher claim amounts, higher income, dominated by surgery claims via Phone.  
- Insights used for potential business strategies like **cross-selling**, **targeted services**, and **risk management**.

### 4. Supervised Learning
- Models trained to predict cluster membership:  
  - **Random Forest Classifier**  
  - **K-Nearest Neighbors (KNN)**  

- **Evaluation Metrics:**  
  - Accuracy  
  - Precision, Recall, F1-score  
  - Confusion Matrix  

- **Hyperparameter Tuning:**  
  - RandomizedSearchCV for Random Forest  
  - GridSearchCV for KNN  

### 5. Model Evaluation
- Both models achieved **near-perfect performance** due to clearly separable clusters.  
- Random Forest maintained 100% accuracy, KNN slightly dropped to 99.89% after tuning.  
- Recommendations: test on **noisy or more complex datasets** to validate generalization.

---

## Technologies Used
- Python 3.12
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn

---





