# Logistic Regression: Airline Passenger Satisfaction Prediction

## Project Overview

This project applies **Logistic Regression** to predict airline passenger satisfaction using survey data. The objective is to classify passengers as **Satisfied** or **Neutral/Dissatisfied** based on demographic information, travel details, and service quality ratings. The project demonstrates the complete machine learning workflow, including data preprocessing, feature engineering, model training, evaluation, interpretation, and business recommendations.

---

## Objectives

* Preprocess and prepare the airline passenger dataset for classification.
* Encode categorical variables into numerical representations.
* Train a Logistic Regression classification model.
* Evaluate the model using multiple performance metrics.
* Identify the key factors influencing passenger satisfaction.
* Provide actionable business recommendations based on the model findings.

---

## Dataset

The dataset contains passenger information, travel characteristics, and service ratings, including:

* Customer Type
* Age
* Type of Travel
* Class
* Flight Distance
* Seat Comfort
* Inflight Entertainment
* On-board Service
* Check-in Service
* Online Boarding
* Arrival and Departure Delays
* Satisfaction (Target Variable)

**Target Variable**

* **0** = Neutral or Dissatisfied
* **1** = Satisfied

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

---

## Data Preprocessing

The following preprocessing steps were performed:

* Loaded and explored the dataset.
* Checked for missing values.
* Replaced missing values in **Arrival Delay in Minutes** using the median.
* Encoded categorical variables using **LabelEncoder**.
* Split the dataset into **80% training** and **20% testing** sets.
* Standardized numerical features using **StandardScaler** to improve model convergence.

---

## Model Development

A **Logistic Regression** classifier was trained using Scikit-learn.

```python
model = LogisticRegression(max_iter=5000)
```

The trained model predicts the probability that a passenger belongs to the **Satisfied** class.

---

## Model Evaluation

### Accuracy

* **82.58%**

### Precision

* **84%**

### Recall

* **84.09%**

### F1-Score

* **84%** (Satisfied)
* **81%** (Neutral/Dissatisfied)

### Confusion Matrix

| Actual               | Predicted Neutral/Dissatisfied | Predicted Satisfied |
| -------------------- | ------------------------------ | ------------------- |
| Neutral/Dissatisfied | 9,425                          | 2,250               |
| Satisfied            | 2,276                          | 12,025              |

The model correctly classified **21,450** out of **25,976** passengers, demonstrating strong and balanced classification performance.

---

## Key Findings

The Logistic Regression coefficients indicate that the strongest positive drivers of passenger satisfaction are:

* Inflight Entertainment
* On-board Service
* Seat Comfort
* Check-in Service
* Ease of Online Booking
* Leg Room Service

Factors associated with lower passenger satisfaction include:

* Disloyal Customer
* Personal Travel
* Economy Class
* Arrival Delay in Minutes

These findings suggest that both service quality and operational efficiency significantly influence customer satisfaction.

---

## Business Recommendations

* Improve in-flight entertainment and onboard services to enhance the passenger experience.
* Invest in seat comfort and streamline online booking and check-in processes.
* Minimize arrival delays through improved operational planning.
* Strengthen customer loyalty programs to improve passenger retention.
* Develop targeted strategies to improve the travel experience for personal and economy-class passengers.

---

## Model Limitations

* Logistic Regression assumes a linear relationship between the predictors and the log-odds of the target variable.
* Label encoding may introduce artificial ordering for nominal categorical variables.
* The model may not capture complex nonlinear relationships or feature interactions.
* Future work could evaluate models such as Random Forest, Gradient Boosting, or XGBoost for improved predictive performance.

---

## Conclusion

The Logistic Regression model successfully predicted airline passenger satisfaction with an overall **accuracy of 82.58%** and strong precision, recall, and F1-score values. The analysis identified customer loyalty, service quality, and operational performance as the primary drivers of satisfaction. These insights can help airlines prioritize service improvements, enhance customer retention, and support data-driven decision-making.

---

## Repository Structure

```text
Logistic_Regression_Airline_Satisfaction/
│
├── logistic_regression_analysis.ipynb
├── README.md
├── requirements.txt
└── dataset/
    └── airline_passenger_satisfaction.csv
```

---

## How to Run the Project

1. Clone the repository.

```bash
git clone https://github.com/your-username/Logistic_Regression_Airline_Satisfaction.git
```

2. Navigate to the project directory.

```bash
cd Logistic_Regression_Airline_Satisfaction
```

3. Install the required libraries.

```bash
pip install -r requirements.txt
```

4. Launch Jupyter Notebook.

```bash
jupyter notebook
```

5. Open **`logistic_regression_analysis.ipynb`** and run all cells.

---

## Author

**Abeeb Masood**
