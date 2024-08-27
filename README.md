# Transaction Fraud Detection

## Project Overview
The **Transaction Fraud Detection** project aims to predict whether a financial transaction is fraudulent or not.

### Problem Statement
Blocker Fraud Company operates on a performance-based model:
- **25%** of the transaction value for correctly identified fraud.
- **5%** of the transaction value for incorrectly identified fraud.
- **100%** reimbursement for legitimate transactions mistakenly flagged as fraud.

With this model, the company needs highly accurate fraud detection to maximize revenue and minimize losses.

### Project Assumptions
Fraud prevention is essential to protect financial institutions and clients. Fraud losses can reach significant figures annually. Investments in security are crucial, as fraud can severely impact financial institutions.

### Solution/Idea
This project involves developing a machine learning model to predict transaction fraud. The steps are as follows:

1. **Data Description**:
   - Collect and study data.
   - Handle missing values.
   - Perform initial data descriptive statistics.

2. **Feature Engineering**:
   - Create a mind map for hypothesis generation and feature creation.
   - Enhance exploratory data analysis (EDA) with new features.

3. **Data Filtering**:
   - Remove irrelevant columns or rows, such as customer IDs or non-human ages.

4. **Exploratory Data Analysis**:
   - Conduct univariate, bivariate, and multivariate analyses.
   - Test hypotheses and explore data relationships.

5. **Data Preparation**:
   - Prepare data for machine learning by encoding, oversampling, subsampling, or rescaling.

6. **Feature Selection**:
   - Use algorithms like Boruta to select relevant features and reduce dimensionality.

7. **Machine Learning Modeling**:
   - Train and validate machine learning models.
   - Apply cross-validation to assess model performance.

8. **Hyperparameter Tuning**:
   - Fine-tune parameters to improve model performance.

9. **Conclusions**:
   - Evaluate model performance on unseen data.
   - Address business questions and demonstrate model applicability.

10. **Model Deployment**:
    - Create a Flask API for model deployment.

### Top 3 Data Insights
1. **Fraud Amounts**:
   - All fraud amounts exceed 10,000. No-fraud amounts are also above 100,000.
    ![image](https://github.com/user-attachments/assets/6512c794-285b-4645-b817-9f99bed6ab12)

2. **Fraud Transaction Methods**:
   - Fraud transactions occur in both transfer and cash-out methods, nearly equally.
    ![image](https://github.com/user-attachments/assets/bd256228-6783-474b-ac9e-ecedbe64296a)

3. **High-Value Transactions**:
   - Transactions over 100,000 occur in transfer, cash-out, and cash-in methods.
     ![image](https://github.com/user-attachments/assets/fb482e2d-6571-48a8-82ed-80506328c740)


### Machine Learning Applied
Cross-validation results for various models with default parameters:

| Model               | Balanced Accuracy | Precision | Recall | F1    | Kappa |
|---------------------|--------------------|-----------|--------|-------|-------|
| Dummy Model         | 0.499 +/- 0.0      | 0.0       | 0.0    | 0.0   | -0.001|
| Logistic Regression | 0.565 +/- 0.009    | 1.0       | 0.129  | 0.229 | 0.228 |
| K Nearest Neighbors | 0.705 +/- 0.037    | 0.942     | 0.409  | 0.568 | 0.567 |
| Support Vector Machine | 0.595 +/- 0.013 | 1.0       | 0.19   | 0.319 | 0.319 |
| Random Forest       | 0.865 +/- 0.017    | 0.972     | 0.731  | 0.834 | 0.833 |
| XGBoost             | 0.88 +/- 0.016     | 0.963     | 0.761  | 0.85  | 0.85  |
| LightGBM            | 0.701 +/- 0.089    | 0.18      | 0.407  | 0.241 | 0.239 |

### Machine Learning Performance
The chosen model, XGBoost, was tuned for optimal performance:

| Metric              | Value                |
|---------------------|----------------------|
| Balanced Accuracy   | 0.881 +/- 0.017      |
| Precision           | 0.963 +/- 0.007      |
| Recall              | 0.763 +/- 0.035      |
| F1                  | 0.851 +/- 0.023      |
| Kappa               | 0.851 +/- 0.023      |

For unseen data:
- **Balanced Accuracy**: 91.5%
- **Precision**: 94.4%
- **Recall**: 82.9%
- **F1**: 88.3%
- **Kappa**: 88.3%


### Conclusions
The model effectively handles the imbalanced data and provides high accuracy in fraud detection.

### Learning Outcomes
- Effective models can be built even with imbalanced classes.
- Models can classify rare classes effectively.

### Future Scope
- Test additional hypotheses.
- Implement oversampling or subsampling techniques to improve model performance.
- Deploy the model on the Heroku platform.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
