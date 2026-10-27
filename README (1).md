# Machine Learning Labs

Weekly lab work for the Machine Learning course (Fall 2026), Sukkur IBA University.

**Author:** Azhar Ali Soomro
**Program:** BS Computer Science (AI Specialization)
**Status:** In progress. New labs are added every week.

---

## About this repository

This repo contains my solved ML lab notebooks. Each lab is a single Jupyter notebook with code, plots, and written observations. Most labs use the Telco Customer Churn dataset, so the results can be compared lab to lab as the models change.

Tools used: Python, Pandas, NumPy, Matplotlib, Seaborn, scikit-learn. Notebooks were run on Kaggle and Google Colab.

---

## Labs completed

| Lab | Topic | Dataset | Notebook |
|-----|-------|---------|----------|
| Lab 2 | Data Cleaning & EDA | Telco Customer Churn | `Lab2_Data_Cleaning_EDA_Template_Solved.ipynb` |
| Lab 3 | Decision Tree Classification | Telco Customer Churn | `lab-3-decision-tree-classification.ipynb` |
| Lab 4 | Random Forest, Cross-Validation, Hyperparameter Tuning | Telco Customer Churn | `Lab4_Model_Comparison_RandomForest_and_Decision_Tree.ipynb` |
| Lab 5 | Linear Regression | House Prices (Kaggle) | `lab-5-advanced-regression-techniques.ipynb`, `linear-regression.ipynb` |
| Lab 6 | Logistic Regression & KNN | Telco Customer Churn | `lab6-telco-churn-logreg-knn-classification__1_.ipynb` |
| Week 7 | Naive Bayes: Spam Detection & Sentiment Analysis | SMS Spam Collection, US Airline Tweets | `spam-detection-and-sentimentanalysis__1___3_.ipynb`, `sms-spam-detection-ml.ipynb`, `us-airline-sentiment-analysis.ipynb` |
| Lab 8 | Support Vector Machines | Telco Customer Churn | `svm-telco.ipynb` |

---

## What each lab covers

### Lab 2: Data Cleaning & EDA
- Defined the business problem (customer churn) and the target variable.
- Audited data quality: missing values, wrong data types, useless columns such as `customerID`.
- Explored the data with plots and wrote an observation for each one.
- The cleaned dataset from this lab is reused in the later labs.

### Lab 3: Decision Tree Classification
- Trained a Decision Tree on the cleaned churn data.
- Showed overfitting with a fully grown tree: training accuracy about 99.8% vs test accuracy about 72.6%.
- Compared different `max_depth` values. Best test accuracy was at depth 6 (about 80.1%).

### Lab 4: Random Forest, Cross-Validation & Tuning
- Compared a Decision Tree baseline against a Random Forest.
- Used 5-fold cross-validation (mean F1: Decision Tree 0.496, Random Forest 0.554).
- Tuned the Random Forest with hyperparameter search. Best parameters: `max_depth=10`, `n_estimators=50`, `min_samples_split=2`.

### Lab 5: Linear Regression (House Prices)
- Predicted `SalePrice` using a subset of numerical and categorical features.
- Evaluated with MAE, MSE, RMSE and R².
- Compared training and testing performance to check for overfitting.

### Lab 6: Logistic Regression & KNN
- Applied feature scaling with `StandardScaler`, fitted on training data only.
- Tuned Logistic Regression with grid search.
- Tested KNN for different values of K.
- Compared four classifiers (Decision Tree, Random Forest, Logistic Regression, KNN) side by side.

### Week 7: Naive Bayes
- **Spam detection:** `CountVectorizer` + `MultinomialNB` on the SMS Spam Collection.
- **Sentiment analysis:** same pipeline on US airline tweets, with URL and @mention cleaning, using only positive and negative tweets.
- Compared Naive Bayes against Logistic Regression on the spam task.

### Lab 8: Support Vector Machines
- Showed why scaling matters for SVM (training time dropped from about 301 s to about 1.4 s after scaling).
- Compared Linear, RBF and Polynomial kernels.
- Tuned `C` and `gamma` with cross-validation.
- Tested class balancing and its effect on the precision/recall trade-off.
- Compared all models trained so far on the same train/test split.

---

## Key results

### Telco Customer Churn (test set, same split across labs)

| Model | Accuracy | Precision | Recall | F1 |
|-------|----------|-----------|--------|-----|
| Decision Tree | 0.716 | 0.466 | 0.460 | 0.463 |
| KNN | 0.753 | 0.536 | 0.535 | 0.535 |
| Random Forest | 0.788 | 0.623 | 0.513 | 0.563 |
| SVM | 0.797 | 0.645 | 0.529 | 0.581 |
| Logistic Regression | 0.804 | 0.648 | 0.575 | 0.609 |

*(From the final comparison table in the Lab 8 notebook. Numbers from earlier labs can differ slightly because of different tuning and splits.)*

### House Prices (Lab 5, test set)

| Metric | Value |
|--------|-------|
| MAE | about 20,652 |
| RMSE | about 33,170 |
| R² | 0.857 |

### Text classification (Week 7)

| Task | Model | Accuracy | Precision | Recall | F1 |
|------|-------|----------|-----------|--------|-----|
| SMS Spam | Multinomial Naive Bayes | 0.984 | 0.985 | 0.893 | 0.937 |
| SMS Spam | Logistic Regression | 0.922 | 0.839 | 0.736 | 0.784 |
| Airline Sentiment | Multinomial Naive Bayes | 0.915 | 0.922 | 0.611 | 0.735 |

---

## Datasets

- Telco Customer Churn: https://www.kaggle.com/datasets/blastchar/telco-customer-churn
- House Prices, Advanced Regression Techniques: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques
- SMS Spam Collection: https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset
- Twitter US Airline Sentiment: https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment

Datasets are not included in this repo. Download them from the links above.

---

## How to run

1. Clone the repository:
   ```bash
   git clone https://github.com/Azharaliii/<repo-name>.git
   ```
2. Install the requirements:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
3. Download the required dataset and update the file path in the first code cells (the notebooks use Kaggle/Colab paths).
4. Open the notebook with Jupyter, or upload it to Kaggle/Colab, and run the cells in order.

---

## Upcoming

More labs will be added here as the course continues.

---

## Contact

- GitHub: [Azharaliii](https://github.com/Azharaliii)
- Kaggle: [azharalisoomro](https://www.kaggle.com/azharalisoomro)
