# Heart-Attack-Risks

## Problem Statement

Heart disease is one of the leading causes of death worldwide, making early detection and prevention a major public health priority. Healthcare datasets often contain numerous demographic, lifestyle, and clinical variables that may influence disease outcomes, making it challenging to determine which predictors are truly significant.

The objectives of this project were to:

* Identify meaningful predictors associated with heart disease.
* Determine which risk factors are statistically significant.
* Build reliable classification and regression models.
* Compare multiple machine learning and statistical approaches.
* Maximize predictive performance on unseen data.
* Evaluate model interpretability and reliability using statistical diagnostics.

By leveraging a large healthcare dataset, this project demonstrates how predictive analytics can support data-driven decision-making in medical research and cardiovascular health assessment.

---

## Methodology

### Dataset

The dataset was obtained from Kaggle and contains:

* 10,000 patient observations
* 21 variables
* 1 binary response variable (Heart Disease Status)
* 20 predictor variables including demographic, behavioral, and clinical health indicators

### Data Preparation

Several preprocessing steps were performed:

* Removed observations containing missing values.
* Converted categorical variables into numerical representations for machine learning algorithms.
* Encoded binary and ordinal categorical variables.
* Split the dataset into:

  * 80% Training Data (7,600 observations)
  * 20% Testing Data (1,900 observations)

### Exploratory Data Analysis (EDA)

To better understand the dataset:

* Examined distributions of all predictors.
* Investigated class balance of the response variable.
* Created histograms and bar charts for quantitative and categorical variables.
* Evaluated potential relationships between predictors and heart disease status.

### Statistical Modeling

This project utilized multiple statistical and machine learning techniques:

#### Regression Models

* Logistic Regression
* LASSO Regression

#### Tree-Based Methods

* Decision Tree
* Bagging
* Random Forest
* XGBoost

#### Classification Methods

* K-Nearest Neighbors (KNN)
* Naive Bayes
* Linear Discriminant Analysis (LDA)
* Quadratic Discriminant Analysis (QDA)

### Model Validation

Several validation and diagnostic procedures were applied:

* Variance Inflation Factor (VIF) analysis to assess multicollinearity.
* Residual diagnostics using randomized quantile residual plots.
* Cross-validation to select optimal LASSO penalty values.
* Confusion matrix evaluation.
* Accuracy, sensitivity, and specificity calculations.
* Feature selection through regularization techniques.

### Tools & Technologies

* R
* RStudio
* Statistical Modeling
* Machine Learning
* Data Visualization
* Regression Analysis
* Classification Modeling

---

## Project Explanation

This project investigated how various health indicators contribute to heart disease risk.

The response variable was:

**Heart Disease Status**

* Yes (Heart Disease)
* No (No Heart Disease)

The predictor variables included:

* Age
* Gender
* Blood Pressure
* Cholesterol Level
* Exercise Habits
* Smoking Status
* Family History of Heart Disease
* Diabetes
* BMI
* High Blood Pressure
* Low HDL Cholesterol
* High LDL Cholesterol
* Alcohol Consumption
* Stress Level
* Sleep Hours
* Sugar Consumption
* Triglyceride Levels
* Fasting Blood Sugar
* CRP Levels
* Homocysteine Levels

### Why Multiple Models?

Different machine learning algorithms capture patterns differently. This project compared several methods to determine:

* Which model achieved the highest predictive performance.
* Which variables were most influential.
* How model complexity affected interpretability.
* Whether feature selection improved prediction quality.

### Feature Selection with LASSO

LASSO regression was used to shrink less important coefficients toward zero and automatically identify influential predictors.

The most influential variables selected by LASSO included:

* Gender
* Blood Pressure
* BMI
* Alcohol Consumption
* Stress Level

### Logistic Regression Analysis

Logistic regression was used to determine statistical significance among predictors.

After assessing assumptions and model diagnostics:

* No concerning multicollinearity was detected.
* Logistic regression assumptions were reasonably satisfied.
* BMI emerged as the only statistically significant predictor at the 5% significance level.

This finding suggests that body mass index has a measurable association with heart disease risk in this dataset.

---

## Results

The project successfully:

* Built multiple predictive models.
* Identified statistically significant predictors.
* Evaluated model performance using classification metrics.
* Applied feature selection techniques.
* Reduced model complexity through LASSO regularization.
* Produced interpretable visualizations and statistical findings.
* Demonstrated the importance of comparing multiple modeling approaches.

### Significant Predictor

The strongest statistically significant predictor identified was:

**BMI (Body Mass Index)**

BMI was the only predictor with a p-value below 0.05 in the full logistic regression model.

### Model Performance Comparison

| Model               | Accuracy   | Sensitivity | Specificity |
| ------------------- | ---------- | ----------- | ----------- |
| Logistic Regression | 79.97%     | 0.00%       | 100.00%     |
| LASSO Regression    | 79.97%     | 0.00%       | 100.00%     |
| Decision Tree       | 79.95%     | 0.00%       | 100.00%     |
| Bagging             | 79.00%     | 1.31%       | 98.49%      |
| Random Forest       | 79.95%     | 0.00%       | 100.00%     |
| XGBoost             | 79.95%     | 0.00%       | 100.00%     |
| KNN                 | 79.95%     | 0.00%       | 100.00%     |
| Naive Bayes         | 79.95%     | 0.00%       | 100.00%     |
| LDA                 | 79.97%     | 0.00%       | 100.00%     |
| QDA                 | **79.99%** | **0.47%**   | **99.91%**  |

### Best Performing Model

Quadratic Discriminant Analysis (QDA) achieved the strongest overall performance:

* Accuracy: 79.99%
* Sensitivity: 0.47%
* Specificity: 99.91%

Although QDA performed best overall, all models struggled to identify positive heart disease cases due to class imbalance within the dataset.

---

## Accuracy Metrics

Model performance was evaluated using several statistical measures.

### Accuracy

Measures the percentage of correct predictions.

Accuracy = (TP + TN) / (TP + TN + FP + FN)

### Sensitivity (Recall)

Measures the ability to correctly identify individuals with heart disease.

Sensitivity = TP / (TP + FN)

### Specificity

Measures the ability to correctly identify individuals without heart disease.

Specificity = TN / (TN + FP)

### Additional Evaluation Techniques

The project also incorporated:

* Predictor Significance Testing
* Residual Analysis
* Cross Validation
* Confusion Matrix Analysis
* Model Comparison Metrics
* Multicollinearity Diagnostics (VIF)

### Evaluation Highlights

* Feature selection simplified models while maintaining performance.
* Multicollinearity was effectively minimized.
* Statistical testing improved model interpretability.
* Visualization techniques improved communication of findings.
* Classification metrics revealed limitations caused by class imbalance.

---

## Lessons Learned

This project provided valuable experience in statistical modeling, machine learning, and healthcare analytics.

### Technical Lessons

* Data cleaning and preprocessing are critical for model reliability.
* Feature selection can improve interpretability without sacrificing performance.
* Multicollinearity can negatively impact regression models and should be assessed before interpretation.
* Model assumptions must be validated before drawing conclusions.
* Accuracy alone can be misleading when classes are imbalanced.

### Statistical Lessons

* Statistical significance does not always translate into predictive power.
* High specificity does not guarantee effective classification.
* Sensitivity is especially important in healthcare applications because missed positive cases can have serious consequences.
* Different algorithms can produce substantially different results on the same dataset.

### Professional Growth

This project strengthened my skills in:

* Regression Modeling
* Logistic Regression
* Machine Learning
* Predictive Analytics
* Statistical Analysis
* Feature Selection
* Model Evaluation
* Data Visualization
* Research Communication
* Healthcare Data Analysis

---

## Future Improvements

Future work could improve predictive performance by:

* Applying class-balancing techniques such as SMOTE.
* Performing hyperparameter optimization.
* Testing additional ensemble learning methods.
* Evaluating ROC-AUC and Precision-Recall curves.
* Exploring deep learning approaches.
* Incorporating larger and more diverse clinical datasets.
* Investigating additional feature engineering techniques.

---

## Conclusion

This project explored the relationship between twenty health-related risk factors and heart disease using both statistical and machine learning methods. Through extensive exploratory analysis, feature selection, model validation, and predictive modeling, BMI emerged as the most significant predictor of heart disease risk. Among all classification approaches, Quadratic Discriminant Analysis achieved the highest predictive accuracy.

The study highlights the importance of rigorous statistical analysis, careful model evaluation, and feature selection when developing predictive healthcare models. These findings contribute to a deeper understanding of cardiovascular risk factors and demonstrate how data-driven approaches can support medical research and decision-making.
