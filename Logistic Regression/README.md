# Logistic Regression
It is a **Supervised Machine Learning Algorithm** used for **Classification** tasks eg: yes/no, 0/1, spam/not spam etc.
Despite its name, it's a classification algorithm not a regression algorithm, because the output is the probability that maps to discrete classes, not the continuous values.

---

## Behind the Scene Working of Logistic Regression
1. **Linear combination** of input features:
$$
y = 𝑤_1 𝑥_1 + … + 𝑤_n 𝑥_n + b
$$
- w: model coefficents (weights)
- x: feature values
- b: bias or intercept term

2. **Apply sigmoid (Logistic) funtion** to convert the output to a probability. 

$$ y = \sigma(z) = \frac{1}{1 + e^{-z}}$$
The **sigmoid function** (also called the logistic function) is the core of logistic regression. It converts any real-valued number into a value between 0 and 1, suitable for interpreting as a probability.

3. **Make Prediction** based on a threshold (ussually 0.5)
- if y ≥ 0.5, predict **class 1**
- Else predict **class 0**

---

## Use Cases
- Spam Email Detection – Classify emails as spam or not spam
- Tumor Classification – Detect if a tumor is malignant or benign
- Customer Churn Detection – Predict if a customer will leave the service

---

## Types of Logistic Regression
Logistic Regression is not limited to binary classification only. It extends to handle multiple classes, even the ordinal relationships.

### 1. Binary Logistic Regression
- Used when the target variable has only two classes.
- Use `Sigmoid Function` for prediction.
- Example: Will customer buy the product? (yes/no)

### 2. Multinomial Logistic Regression
- Used when there are more than two classes in the target variable.
- The `Softmax Function` used for the prediction.
$$ 
softmax(x_i) = \frac{e^{x_i}}{\sum_{j} e^{x_j}} 
$$
- Example: predict one of 10-digits (0-9) based on the image classification.

### 3. Ordinal Logistic Regression
- Used when the target variable has ordered categories.
- Example: Rating levels (high, medium, low).


---

## Key Assumptions of Logistic Regression
1. **Binary or categorical outcome**: The dependent variable should be binary or categorical (for multinomial/ordinal types).
2. **Linearity of logit**: Logistic regression assumes a linear relationship between the log-odds of the dependent variable and the independent variables.
3. **No multicollinearity**: Independent variables should not be highly correlated with each other.
4. **Independent Observations**: Each observation should be independent of others (no duplicate or time-dependent records unless explicitly modeled).
5. **Large sample size**: Logistic regression performs better with large datasets to provide stable estimates.

---

