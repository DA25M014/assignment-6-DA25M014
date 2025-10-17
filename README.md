🧾 [DA5401] DA Lab – Assignment 6 – DA25M014 , Name - Jigarahemad K Shaikh , Roll Number: DA25M014

**File needed for Evaluation - "DA5401_DA25M014_ASSIGNMENT_6_Final_Notebook.ipynb"**


Title: Credit Risk Assessment – Missing Data Imputation & Classification
Date: 17 Oct 2025

📂 File Required for Evaluation

Notebook: DA5401_DA25M014_Assignment6_Final_Notebook.ipynb

This notebook contains complete preprocessing, imputation, modeling, and analytical discussion for the UCI Credit Card Default Clients Dataset.

⚙️ Libraries Used

pandas, numpy – data handling and numerical computation

matplotlib, matplotlib.patches, matplotlib.colors – custom visualizations

seaborn – color-blind-friendly statistical plots

scikit-learn – data preprocessing, imputation models, and Logistic Regression

StandardScaler, train_test_split, KNNImputer, LinearRegression, LogisticRegression, classification_report, roc_curve, auc

warnings, random, scipy.stats – utility modules

🎨 Color Palettes & Colormaps

Palettes: colorblind, Set2, muted, husl, Spectral, and Paul Tol (TOL Colors)

Colormaps: Spectral, coolwarm, viridis (for heatmaps and density plots)

Accessibility: All plots are color-blind friendly and use pattern fills (////, xxxx) with clear legends.

🧠 Assignment Overview

This project evaluates how different missing-data imputation strategies influence the performance of a credit risk classification model (Logistic Regression).
The study uses the UCI Credit Card Default Clients Dataset, simulating real-world missingness and exploring four distinct data handling approaches.

🔧 Workflow Summary
Part A – Data Preprocessing and Imputation

Artificial Missingness:

Introduced ≈ 5% MAR (Missing At Random) values in AGE, BILL_AMT1, and BILL_AMT2.

Imputation Strategies:

Model	Approach	Description
A	Median Imputation	Baseline using robust central tendency against outliers
B	Linear Regression Imputation	Predicts missing values via linear feature relationships
C	Non-Linear (KNN Regression)	Captures complex patterns and local structure
D	Listwise Deletion	Removes rows containing missing data (entirely)
Part B – Model Training and Evaluation

Data split into 80% training / 20% testing, with stratified sampling to preserve class balance.

All features standardized using StandardScaler.

Logistic Regression trained and evaluated for each dataset.

Metrics computed: Accuracy, Precision, Recall, F1-Score, and ROC AUC.

Visual comparisons include grouped bar charts and ROC curves with distinct color and pattern styles for accessibility.

Part C – Comparative Analysis & Discussion
Performance Highlights
Metric	Best Performer	Key Takeaway
Accuracy	≈ 81% (all models similar)	Equal overall correctness
Precision	Model D	Fewer false positives but misses defaults
Recall	Models A–C	Better at detecting true defaulters
F1-Score	Models A & B	Best balance of precision/recall
Weighted F1	Models A–C	Consistent class-balanced performance
⚖️ Trade-Off Analysis: Listwise Deletion vs Imputation

Listwise Deletion reduces dataset diversity and recall due to loss of information.

Imputation Models (A–C) retain complete records, reducing variance and bias.

Even with minor imputation noise, larger training samples yield better generalization.

🧩 Linear vs Non-Linear Regression for Imputation

Linear Regression Imputation (B): Efficient and interpretable for linear relations (e.g., AGE vs LIMIT_BAL).

KNN Imputation (C): Captures non-linear and local patterns, reflecting real financial behaviors.

Result: Model C offered superior recall and stability for minority (default) class.

🧭 Recommended Strategy
Method	Pros	Cons	Verdict
Median Imputation (A)	Simple, robust	Ignores relationships	Good baseline
Linear Imputation (B)	Correlation-aware	Assumes linearity	Good for structured numeric data
KNN Imputation (C)	Captures non-linear patterns	Computationally heavier	Best overall
Listwise Deletion (D)	Easy to apply	High information loss	Not recommended

Final Recommendation: Use Non-Linear (KNN) Regression for robust credit risk imputation when fairness and accuracy are critical.

💡 Insights & Conclusion

Imputation > Deletion: Retaining records enhances learning stability and model recall.

Median Imputation is a dependable baseline, while KNN is ideal for production-grade models.

Listwise Deletion sacrifices valuable signal and underrepresents important client segments.

Model C (KNN) aligns best with the non-linear, multi-dimensional nature of financial behavior.

“In credit risk modeling, intelligent imputation is not just a data cleaning step — it’s a strategic decision that shapes model fairness, accuracy, and business impact.”

🧭 Summary (High-Level)
Section	Focus	Outcome
Part A	Data Preparation & Imputation	4 datasets created (A–D) with different strategies
Part B	Model Training	Logistic Regression trained on each dataset
Part C	Result Analysis	Compared Accuracy, F1, ROC, and Interpretability
Part C2	Efficacy Discussion	Listwise Deletion vs Imputation trade-off
Part C3	Recommendation	KNN Imputation identified as the most effective approach
🧩 Final Takeaway

Precision in Imputation = Precision in Prediction.
Thoughtful missing-data treatment translates directly to trustworthy and fair credit risk models — ensuring both analytical rigor and ethical decision-making in data-driven banking.

