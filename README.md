# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the required data manipulation and machine learning libraries, then load the dataset.

### Step2
Separate the dataset into independent input features (X) and the dependent target variable (y).

### Step3
Initialize the linear regression model and train it by fitting the feature and target data.

### Step4
Extract and display the model's calculated regression coefficients and intercept.

### Step5
Pass new input values into the trained model to predict and display the estimated output.

## Program:
#Developed by:Harish Amal S

#Referance Number:26014406

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

## Output:

<img width="1195" height="667" alt="image" src="https://github.com/user-attachments/assets/cf7549b0-20e6-4537-9ba9-75571119df1d" />

<img width="833" height="85" alt="image" src="https://github.com/user-attachments/assets/287ce6b1-ce3b-4432-ad5e-5abdbfc93cea" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
