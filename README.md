# ProstateEnsembleNet

### A Novel Framework Integrating Epidemiological Features and Machine Learning Models for Prostate Cancer Detection on Imbalanced Dataset

---

##  Published Paper

> **Muhammad Mohsin, Ayesha Anwar, Muhammad Shadab Alam Hashmi, Silvia Aparicio Obregon, Ruben Calderon Iglesias, Nagwan Abdel Samee, Imran Ashraf**
>
> *"A Novel Framework Integrating Epidemiological Features and Machine Learning Models for Prostate Cancer Detection on Imbalanced Dataset"*
>
> **International Journal of Computational Intelligence Systems**, Springer Netherlands, 2026.
>
>  **DOI:** [10.1007/s44196-026-01489-4](https://doi.org/10.1007/s44196-026-01489-4)
>
>  **PDF:** [Download Paper](https://link.springer.com/content/pdf/10.1007/s44196-026-01489-4.pdf)

---

##  Overview

Prostate cancer represents a major health issue worldwide, where traditional biopsy-based diagnostics are often limited by patient discomfort, bias, subjectivity, and sampling inaccuracies. This study introduces the **ProstaEnsembleNet** framework, which incorporates machine learning models in an ensemble approach to detect prostate cancer early by utilizing diverse epidemiological features, minimizing geographic and racial disparities.

The designed ensemble learning integrates multiple machine learning and deep learning models, with **logistic regression** serving as the meta-learner. To address data imbalance, the **Synthetic Minority Oversampling Technique (SMOTE)** is applied to the training dataset.

![Proposed Methodology](Prostate%20methodology.jpeg)

---

##  Key Results

Using a prostate cancer dataset containing **29 clinical attributes**, the proposed ensemble approach achieved superior performance:

| Metric    | Score     |
|-----------|-----------|
| **F1 Score**  | 91.42%    |
| **Recall**    | 98.02%    |
| **PR-AUC**    | 86.32%    |

---

##  Models Used

### Base Learners (Machine Learning)
- Gradient Boosting (GB)
- Random Forest (RF)
- Gaussian Naive Bayes (GNB)
- Extreme Gradient Boosting (XGBoost)
- Support Vector Machines (SVM)
- Light Gradient Boosting Machines (LightGBM)
- K-Nearest Neighbors (KNN)

### Deep Learning Models
- TabNet
- Multilayer Perceptron (MLP) — PyTorch

### Ensemble Strategies
- **Stacking Classifier** — with Logistic Regression as meta-learner
- **Voting Classifier**

### Imbalanced Data Handling
- SMOTE (Synthetic Minority Oversampling Technique)
- 
---

##  Repository Structure

```
ProstaEnsembleNet/
├── ProstaEnsembleNet.ipynb     # Main Jupyter Notebook (full pipeline)
├── requirements.txt            # Python dependencies
├── .gitignore                  # Git ignore rules
└── README.md                   # This file
```

---

##  Installation & Setup

### Prerequisites
- Python 3.8+
- pip

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run the Notebook

```bash
jupyter notebook ProstaEnsembleNet.ipynb
```

> **Note:** The notebook was originally developed and executed on **Google Colab**. It can be run locally or uploaded to Colab for GPU-accelerated deep learning experiments.

---

##  Dataset

The study uses a prostate cancer dataset containing **30 features** (including Patient ID) and **29 clinical attributes**, covering epidemiological and screening-related features such as:

- **Demographics:** Age, Race/Ethnicity, Family History
- **Clinical Indicators:** PSA Level, DRE Result, Biopsy Result
- **Symptoms:** Difficulty Urinating, Weak Urine Flow, Blood in Urine
- **Lifestyle Factors:** Smoking Status, Exercise Habits, Alcohol Consumption
- **Comorbidities:** Hypertension, Diabetes, Cholesterol Level
- **Screening & Follow-up:** Screening Age, Follow-Up Required, Prostate Volume
- **Genetic Factors:** Genetic Risk Factors, Previous Cancer History

---

##  Methodology

1. **Data Preprocessing** — Label encoding, feature scaling (StandardScaler & MinMaxScaler), feature selection (Chi-squared test)
2. **Data Balancing** — SMOTE applied to training data to address class imbalance
3. **Model Training** — Individual ML/DL models trained and evaluated using stratified K-fold cross-validation
4. **Ensemble Learning** — Stacking and Voting classifiers to combine base learner predictions
---

##  License

© 2026 The Author(s). Published by Springer Netherlands.

---

##  Contact

For questions or collaboration, please reach out to the corresponding authors:

- **Muhammad Mohsin** — mohsinramzan999@gmail.com
- **Ayesha Anwar** — hayesha1744@gmail.com
