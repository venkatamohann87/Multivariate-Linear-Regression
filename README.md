# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>Import Libraries and Load Data

Import necessary libraries (pandas, sklearn.linear_model) and read the dataset using pandas.read_csv.



### Step2
<br>Select Features and Target

Choose the independent variables (features: Weight and Volume) and the dependent variable (target: CO2).

### Step3
<br>Train the Linear Regression Model

Initialize a linear regression model and fit it using the selected features and target.

### Step4
<br>Display Model Parameters

Output the model's coefficients and intercept, which define the linear relationship.

### Step5
<br>Predict CO2 Emissions

Create a new input with specific values for weight and volume, and use the trained model to predict the corresponding CO2 emission.



## Program:
```

import pandas as pd
from sklearn import linear_model
df = pd.read_csv("C:\\Users\\admin\\Downloads\\carsemission (1).csv")
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

![image](https://github.com/user-attachments/assets/b3edc56a-0a85-4788-a06a-c4c117d32441)


<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
