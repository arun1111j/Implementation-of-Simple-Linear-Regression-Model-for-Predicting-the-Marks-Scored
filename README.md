# Ex 02 -  Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and read the dataframe.
2. Assign hours to X and scores to Y.
3. Implement training set and test set of the dataframe
4. Plot the required graph both for test data and training data.
5. Find the values of MSE , MAE and RMSE.
## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Arun.J
RegisterNumber:2122222040015

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.metrics import mean_absolute_error,mean_squared_error
df=pd.read_csv('student_scores.csv')
print(df)
df.head(0)
df.tail(0)
print(df.head())
print(df.tail())
x = df.iloc[:,:-1].values
print(x)
y = df.iloc[:,1].values
print(y)

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=1/3,random_state=0)
from sklearn.linear_model import LinearRegression
regressor = LinearRegression()
regressor.fit(x_train,y_train)
y_pred = regressor.predict(x_test)
print(y_pred)
print(y_test)


#Graph plot for training data
plt.scatter(x_train,y_train,color='black')
plt.plot(x_train,regressor.predict(x_train),color='purple')
plt.title("Hours vs Scores(Training set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()


#Graph plot for test data
plt.scatter(x_test,y_test,color='red')
plt.plot(x_train,regressor.predict(x_train),color='blue')
plt.title("Hours vs Scores(Testing set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()
mse=mean_absolute_error(y_test,y_pred)
print('MSE = ',mse)
mae=mean_absolute_error(y_test,y_pred)
print('MAE = ',mae)
rmse=np.sqrt(mse)
print("RMSE= ",rmse)
*/

```

## Output:

![Screenshot 2023-08-26 133011](https://github.com/arun1111j/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/128461833/37fdc10d-e77a-4684-b51a-30dd67d87952)
![Screenshot 2023-08-26 133038](https://github.com/arun1111j/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/128461833/5149b2e8-87d3-4092-9e2c-a1e04582a534)
![Screenshot 2023-08-26 133052](https://github.com/arun1111j/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/128461833/3332bb63-40ca-47af-808a-b13332b4aaa3)
![Screenshot 2023-08-26 133328](https://github.com/arun1111j/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/128461833/574c100c-cb49-4fbe-859b-47abc348693c)
![Screenshot 2023-08-26 133334](https://github.com/arun1111j/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/128461833/037b8754-fc45-45ef-aecc-657efbc71bf8)
![Screenshot 2023-08-26 133341](https://github.com/arun1111j/Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored/assets/128461833/7a33bd67-c3d4-49e4-bd3e-3d546acf7629)




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
