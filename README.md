# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
1.Import libraries and load the dataset using pd.read_csv().

### Step2
2.Inspect the dataset using info(), head(), and tail().

### Step3
3.Define features (x) and target (y) from the dataset.

### Step4
4.Train the LinearRegression model with fit().

### Step5
5.Retrieve coefficients, intercept, and predict CO2 for new input using predict().

## Program:
```
import pandas as pd
from sklearn.linear_model import LinearRegression
df = pd.read_csv('carsemission.csv')
df.info()
df.head()
df.tail()
x=df[['Weight','Volume']]
y=df['CO2']
model=LinearRegression()
model.fit(x,y)
print("\nCoefficient:")
print(model.coef_,"\n")
print("Intercept:")
print(model.intercept_,"\n")
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
prediction = model.predict(input_data)
pre=model.predict(input_data)
print("Predicted CO2 for the corresponding weight and volume")
print(pre)

```
## Output:

![image](https://github.com/user-attachments/assets/9613cc1a-b7f8-4f35-9fe4-d8efebd16876)


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
