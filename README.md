# Loan Data Analysis Project

This project aims to analyze a loan dataset spanning from 2007 to 2014, applying various machine learning models to predict loan outcomes, such as whether a loan will default. The focus is on comparing the performance of different models, particularly Logistic Regression and K-Nearest Neighbors (KNN), for their ability to correctly classify "Good Loan" and "Bad Loan" outcomes.

## Project Overview
- **Data Source:** [loan_data_2007_2014.csv](https://binusianorg-my.sharepoint.com/personal/alisha_saadiya_binus_ac_id/_layouts/15/guestaccess.aspx?share=EWVgxxcjFW1Dgt2UInm-B-kB8jLgIqd2AICcL_1jP5598A&e=mmeQ7T)
- **Number of Rows:** 466,285
- **Number of Features:** 75 columns, including loan characteristics such as loan amount, interest rate, installment, grade, and more.

## Key Steps in the Project
1. Data Understanding and Preprocessing:
    - Exploration of the dataset including understanding distributions and identifying missing values.
    - Features were selected and cleaned to improve the performance of machine learning models.
    - Data was balanced using techniques like oversampling due to an imbalance between "Good Loan" and "Bad Loan" categories.

2. Modeling and Evaluation:
    - Two primary machine learning models were evaluated:
        1. Logistic Regression
        2. K-Nearest Neighbors (KNN)
    - Models were evaluated based on precision, recall, confusion matrix, and other key metrics to determine their predictive performance.

## Results Summary
### Logistic Regression
- Precision for Bad Loan: Logistic Regression performs better in terms of precision when identifying "Bad Loans". This means the model is more conservative in classifying loans as "Bad", leading to fewer False Positives.
- Recall for Good Loan: Logistic Regression achieves perfect recall for "Good Loan", meaning all "Good Loans" are correctly classified. However, the recall for "Bad Loan" is lower, meaning some "Bad Loans" are missed by the model.

### K-Nearest Neighbors (KNN)
- Recall for Bad Loan: KNN performs better in terms of recall for "Bad Loans". It is able to correctly identify more "Bad Loans" compared to Logistic Regression. However, this comes at the cost of having more False Positives for "Good Loans", where some loans classified as "Bad" are actually "Good".

### Overall Comparison
- Logistic Regression is preferable if the goal is to reduce False Positives for "Good Loans" and maintain high precision for "Bad Loans".
- KNN is more suitable if the priority is to reduce False Negatives for "Bad Loans", meaning you want to identify as many "Bad Loans" as possible, even if it means having more False Positives for "Good Loans".
Both models perform well overall, and the choice between the two depends on whether it is more important to minimize False Negatives or False Positives for "Bad Loans."

## Technical Requirements
To run the analysis and models, you will need the following Python packages:

- `pandas `
- `numpy `
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `imbalance-learn`

You can install the required packages by running:

`pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn`

## How to Run the Project
1. Clone the repository.
2. Ensure you have the required Python packages installed.
3. Place the dataset [loan_data_2007_2014.csv](https://binusianorg-my.sharepoint.com/personal/alisha_saadiya_binus_ac_id/_layouts/15/guestaccess.aspx?share=EWVgxxcjFW1Dgt2UInm-B-kB8jLgIqd2AICcL_1jP5598A&e=mmeQ7T)
    - **Number of Rows:** 466,285 in the root directory.
4. Open the Jupyter notebook and run the cells to execute the analysis and modeling.

## Project Goals
- Explore the characteristics of loans from 2007 to 2014.
- Build models to predict loan outcomes, focusing on minimizing misclassifications.
Evaluate model performance using confusion matrices, precision-recall curves, and ROC curves.
