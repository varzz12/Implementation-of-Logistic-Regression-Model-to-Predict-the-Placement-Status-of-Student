# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Data Preprocessing: Clean the dataset by handling missing values and encoding categorical variables (like Gender or Stream). Scale the features (GPA, Test Scores) so they fall within a similar range.
2.Model Initialization: Define the Logistic Regression model. This model uses the Sigmoid Function to map any real-valued number into a probability value between 0 and 1.

3.Training: Feed the training data (Xtrain, ytrain) into the model.The algorithm uses an optimization iterative process (like Gradient Descent) to find the best weights for each input feature.
4.Prediction & Evaluation: Use the trained model on the test set to predict placement. Evaluate the performance using an Accuracy Score or a Confusion Matrix. 

## Program:
```
/*
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report
import matplotlib.pyplot as plt
import seaborn as sns

data = pd.read_csv("Placement_Data.csv")   

data = data.drop(["sl_no", "salary"], axis=1)

data["status"] = data["status"].map({"Placed": 1, "Not Placed": 0})

X = data.drop("status", axis=1)
y = data["status"]

X = pd.get_dummies(X, drop_first=True)

print("\nAfter Encoding:")
print(X.head())

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

X_train, X_test, y_train, y_test = train_test_split(
    X_scaled, y, test_size=0.2, random_state=42
)

model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)

y_pred = model.predict(X_test)
y_prob = model.predict_proba(X_test)[:, 1]

print("\nAccuracy:", accuracy_score(y_test, y_pred))

print("\nClassification Report:")
print(classification_report(y_test, y_pred))

cm = confusion_matrix(y_test, y_pred)
sns.heatmap(cm, annot=True, fmt="d", cmap="Blues")
plt.xlabel("Predicted")
plt.ylabel("Actual")
plt.title("Confusion Matrix - Placement Prediction")
plt.show()
Developed by: 
RegisterNumber:  
*/
```

## Output:
<img width="713" height="736" alt="Screenshot 2026-01-31 141318" src="https://github.com/user-attachments/assets/a17c0860-0882-4b90-9b10-3f3076f3e670" />
<img width="707" height="586" alt="Screenshot 2026-01-31 141333" src="https://github.com/user-attachments/assets/4318319a-18cb-4bf5-a497-599e5e15bc7a" />




## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
