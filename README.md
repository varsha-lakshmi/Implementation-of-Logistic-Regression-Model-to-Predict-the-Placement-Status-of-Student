# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: VARSHA S
RegisterNumber:  212225040482

import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report


data = {
    'cgpa': [6.8, 5.9, 7.5, 8.2, 6.1, 9.0, 5.2, 8.5, 7.8, 6.5, 7.1, 8.0],
    'iq': [120, 105, 130, 145, 110, 150, 95, 140, 135, 115, 125, 138],
    'placement_status': [1, 0, 1, 1, 0, 1, 0, 1, 1, 0, 1, 1]
}
df = pd.DataFrame(data)

print("Dataset Preview:")
print(df.head(), "\n")

X = df[['cgpa', 'iq']]
y = df['placement_status']


X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)


scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)

model = LogisticRegression()
model.fit(X_train_scaled, y_train)

y_pred = model.predict(X_test_scaled)


accuracy = accuracy_score(y_test, y_pred)
conf_matrix = confusion_matrix(y_test, y_pred)
class_report = classification_report(y_test, y_pred, zero_division=0)

print("--- Model Evaluation ---")
print(f"Accuracy Score: {accuracy * 100:.2f}%\n")
print("Confusion Matrix:")
print(conf_matrix, "\n")
print("Classification Report:")
print(class_report)


new_student = [[7.9, 132]]
new_student_scaled = scaler.transform(new_student)
prediction = model.predict(new_student_scaled)

print("--- New Prediction ---")
if prediction[0] == 1:
    print("Prediction for new student: PLACED")
else:
    print("Prediction for new student: NOT PLACED")

*/

```

## Output:


<img width="645" height="572" alt="Screenshot 2026-08-17 211628" src="https://github.com/user-attachments/assets/36792214-fe00-4502-a2de-45c49714024a" />



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
