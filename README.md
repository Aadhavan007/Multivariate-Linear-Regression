# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
import pandas as pd
<br>

### Step2
read and load csv file
<br>


### Step3
import linear_model
<br>

### Step4
Train model
<br>

### Step5
Predict Output
<br>

## Program:
```
'''
DEVELOPED BY: M AADHAVAN NAGARAJAN
REGISTER NUMBER: 212225040001
'''

# Dataset Setup - Run this cell before starting the experiment

import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")


import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)





```
## Output:

<br>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/34d1cafa-ade2-467e-ab6c-8e6a9f52ee51" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
