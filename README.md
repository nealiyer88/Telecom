# Telecom Customer Churn Prediction Project

## Overview
This project focuses on predicting customer churn for **SyriaTel**, a telecommunications company. By identifying customers likely to churn, the company can take proactive measures to improve retention, ultimately reducing churn rates and increasing profitability. This project builds a machine learning classification model to predict which customers are at the highest risk of leaving, enabling the business to make data-driven decisions for customer retention strategies.

## Project Goals
The primary goals of the project are:
- **Predict customer churn** using historical customer data.
- **Provide actionable insights** that can help reduce customer churn through targeted marketing and retention efforts.
- **Evaluate model performance** using metrics that align with the business objectives, particularly focusing on precision to minimize false positives in churn prediction.

---

## Repository Structure

- **`notebook.ipynb`**: The Jupyter notebook containing the code, data analysis, model building, and evaluation.
- **`README.md`**: This file, providing an overview of the project and the repository structure.
- **`data/`**: Folder containing the raw data used in the project (if not linked externally).
- **`images/`**: Folder containing any images or plots used in the project.

---

## Business Understanding
The business problem revolves around **customer churn**—the loss of subscribers over time. Churn has a significant financial impact on telecommunications companies like SyriaTel, as acquiring new customers is typically more expensive than retaining existing ones.

**Stakeholders**:
- **SyriaTel**'s **marketing** and **customer service** departments will be the primary users of the model. These teams can use churn predictions to target at-risk customers with retention offers, discounts, or improved service.

---

## Data Understanding (Updated)

The dataset contains customer data, including:
- **Demographic information** (e.g., gender, age).
- **Contract details** (e.g., type, tenure, payment method).
- **Service usage** (e.g., number of calls, internet usage).
- **Churn indicator** (whether the customer has churned or not).

### Key Features:

From the Random Forest model, the following were identified as the **most important features** for predicting customer churn:

1. **Total Day Charge**: This is the most influential factor, suggesting that customers with higher day charges are more likely to churn.
2. **Total Day Minutes**: The amount of time customers spend on calls during the day is also highly predictive of churn.
3. **Customer Service Calls**: The number of calls made to customer service is a key indicator, likely reflecting customer dissatisfaction.
4. **Total Evening Minutes**: How much time customers spend on calls during the evening also plays a role in predicting churn.
5. **International Plan**: Whether or not a customer is on an international plan significantly influences churn, with both "Yes" and "No" options appearing in the top features.
6. **Total International Calls**: The number of international calls a customer makes is a predictor of churn.
7. **Total Evening Charge**: Charges for evening calls also have a moderate impact on churn prediction.
8. **Total International Charge**: This feature reflects how much customers are being charged for international calls.
9. **Total International Minutes**: The number of minutes spent on international calls is also a relevant feature.

---

## Data Preparation
Data preparation steps included:
1. **Handling missing values** to ensure completeness.
2. **Feature engineering**, such as creating dummy variables for categorical features (e.g., contract type).
3. **Data scaling** where necessary to ensure model compatibility.

These steps were taken to ensure the data is suitable for the machine learning models and are fully documented in the notebook.

---

## Modeling
The modeling process followed an **iterative approach**:
1. **Baseline Model**: A simple Logistic Regression model was used as a starting point.
   - **Accuracy**: 0.86
   - **Precision for 'Churn' class**: 0.54
   - **Recall for 'Churn' class**: 0.26
   - **F1 Score for 'Churn' class**: 0.35

2. **Hypertuned Random Forest Model**: After baseline performance was evaluated, a Random Forest model was built and hypertuned for optimal performance.
   - **Threshold tuning** was performed to maximize precision while balancing recall for the churn class.
   - **Accuracy**: 0.95
   - **Precision for 'Churn' class**: 0.91
   - **F1 Score for 'Churn' class**: 0.80

This model was chosen as the final model because it provided the best balance of high precision and good recall, which aligns with the business need to minimize false positives.

---

## Evaluation
The final model was evaluated using:
- **Precision**: Prioritized to avoid false positives and minimize unnecessary interventions with customers who are not at risk of churning.
- **F1 Score**: Used to balance precision and recall for an overall performance metric.
  
Evaluation on the **holdout test set** confirmed that the model generalizes well to unseen data, providing robust predictions for use in SyriaTel's customer retention strategy.

---

## Code Quality
The code in this project follows professional standards:
- **PEP 8** guidelines were adhered to, ensuring the code is clean and readable.
- Comments and docstrings are included to explain key steps.
- Repetitive code was minimized using functions and loops where applicable.

---

## GitHub Repository
This project repository demonstrates best practices:
- **README.md** file summarizing the project.
- **Organized folder structure** with clear naming conventions.
- **Regular commits** with descriptive messages reflecting the project's development process.

---

## Conclusion
This project demonstrates how machine learning can provide valuable insights for predicting customer churn. By building a high-performing model, SyriaTel can better allocate resources towards retaining customers who are at risk of leaving, ultimately improving business outcomes. The model is ready to be deployed and integrated into the company's operations for ongoing churn prediction.

---

## Instructions for Running the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/nealiyer88/Telecom
