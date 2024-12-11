# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the `pandas` module and `linear_model` from `sklearn`.

### Step2
Use `pd.read_csv` to read the CSV file

### Step3
Create a regression model using `linear_model.LinearRegression()` and assign it to the variable `regr`.

### Step4
Retrieve the coefficients with `regr.coef_` and the intercept with `regr.intercept_`. Use `regr.predict()` to get the predicted results.

### Step5
Print the output and conclude the program.

## Program:
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:',regr.intercept_)
predictedCO2 = regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume',predictedCO2)
```
## Output:

![image](https://github.com/user-attachments/assets/2b22eb94-8f18-4bab-a2ca-3d5f9e6e38fa)

### Insert your output

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
