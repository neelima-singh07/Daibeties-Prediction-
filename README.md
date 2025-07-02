# Diabetes Prediction 

## Overview

This project presents a machine learning approach to predict the likelihood of diabetes in individuals, using a real-world dataset sourced from Kaggle. We explore and compare the performance of two popular classification algorithms: **K-Nearest Neighbors (KNN)** and **Logistic Regression**. The results and visualizations provided offer insights into the strengths and decision boundaries of each model.

---

## Dataset Description

The dataset, obtained from Kaggle, consists of diagnostic measurements for female patients of at least 21 years old. The features include:

- **Pregnancies**: Number of times pregnant
- **Glucose**: Plasma glucose concentration (mg/dL)
- **Blood Pressure**: Diastolic blood pressure (mm Hg)
- **Skin Thickness**: Triceps skin fold thickness (mm)
- **Insulin**: 2-Hour serum insulin (mu U/ml)
- **BMI**: Body mass index (weight in kg/(height in m)^2)
- **Diabetes Pedigree Function**: Likelihood of diabetes based on family history
- **Age**: Patient age (years)
- **Outcome**: Target variable (1 = diabetes, 0 = non-diabetic)

The dataset is a standard benchmark for binary classification in healthcare, particularly for early detection of diabetes.

---

## Methodology

1. **Data Preprocessing**
   - Handled missing or anomalous values by imputing or removing them as appropriate.
   - Standardized features to ensure fair comparison and optimal model performance.
   - Split the data into training and test sets to assess generalizability.

2. **Model Selection & Training**
   - **K-Nearest Neighbors (KNN)**: A non-parametric, instance-based learning algorithm that classifies based on the majority label among the k-nearest data points.
   - **Logistic Regression**: A linear model suitable for binary classification, modeling the probability that an input belongs to the positive class.

3. **Evaluation**
   - Model performance was measured using accuracy on the test set.
   - Visualizations of the decision boundaries were generated for both models, using "Pregnancies" and "Glucose" as example features.

---

## Results

| Model                  | Accuracy  |
|------------------------|-----------|
| Logistic Regression    | **79.8%** |
| K-Nearest Neighbors    | 78.5%     |

- **Logistic Regression achieved the best performance** with an accuracy of 79.8%, marginally outperforming KNN.

### Visualization

The following plots illustrate the decision regions and predictions on the training set:

#### Logistic Regression (Training set)
![logistic](https://github.com/user-attachments/assets/dd1ce63d-8e35-4b41-9a00-99d57088e8b0)


#### KNN (Training set)
![KNN](https://github.com/user-attachments/assets/0513ce27-dca1-4a42-b5d2-5bf434a5e0e3)


- **Red region/points**: Classified as non-diabetic (0)
- **Green region/points**: Classified as diabetic (1)
- The plots highlight how Logistic Regression produces a linear separation, while KNN forms more complex, non-linear boundaries.

---

## Interpretation & Discussion

- Both models provide reasonable predictive performance, demonstrating the feasibility of early diabetes detection using simple medical attributes.
- Logistic Regression, although simpler, yielded slightly better accuracy and more interpretable decision boundaries.
- KNN captured more complex patterns but may be more sensitive to noise and data distribution.

### Professional Insights

- **Model choice in healthcare**: While KNN can identify local patterns, Logistic Regression is often preferred for its interpretability and reliability, especially when clear risk factor relationships are desired.
- **Feature importance**: Further analysis (not shown here) can be performed to quantify which features most influence the prediction, aiding in clinical understanding.

---

## How to Run

1. **Clone the repository.**
2. **Install dependencies:**  
   ```
   pip install -r requirements.txt
   ```
3. **Run the analysis script:**  
   ```
   python diabetes_prediction.py
   ```

---

## Conclusion

This study demonstrates the application of machine learning for diabetes prediction using a widely-used public dataset. With careful preprocessing and model selection, we achieve near 80% accuracy, showing promise for data-driven support in medical diagnostics. The associated code and visualizations provide a starting point for further exploration or deployment in real-world scenarios.

---


