# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the standard Libraries.

2.Set variables for assigning dataset values.

3.Import linear regression from sklearn.

4.Assign the points for representing in the graph.

5.Predict the regression for marks by using the representation of the graph.

6.Compare the graphs and hence we obtained the linear regression for the given datas.
## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: RADHIMEENA M
RegisterNumber:212223040159

import numpy as np
import pandas as pd
from sklearn.metrics import mean_absolute_error,mean_squared_error
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

dataset = pd.read_csv('/content/student_scores (1).csv')
print(dataset.head())
print(dataset.tail()

dataset.info()

x = dataset.iloc[:,:-1].values
print(x)
Y = dataset.iloc[:,-1].values
print(Y)

x_s=x.shape
y_s=Y.shape
print(x_s)
print(y_s)

x_train,x_test,y_train,y_test = train_test_split(x,Y,test_size=1/3,random_state=1)
print(x_train.shape)
print(x_test.shape)
print(y_train.shape)
print(y_test.shape)

reg=LinearRegression()
reg.fit(x_train,y_train)
y_pred=reg.predict(x_test)
print(y_pred)
print(y_test)

mse=mean_squared_error(y_test,y_pred)
mae=mean_absolute_error(y_test,y_pred)
rmse=np.sqrt(mse)
print('MAE=',mae)
print('MSE=',mse)
print('RMSE=',rmse)

plt.scatter(x_test,y_test,color="blue")
plt.plot(x_test,y_pred,color="red")
plt.show()
*/
```

## Output:
![image](https://github.com/user-attachments/assets/2ef66e64-21cf-41e7-bcbc-001f7e7c01cb)

 ![image](https://github.com/user-attachments/assets/48c59365-11c8-4580-a227-dbf96ab42793)
 
![image](https://github.com/user-attachments/assets/69d36bb4-5ff3-45f8-a48f-a48ddbda7caa)

![image](https://github.com/user-attachments/assets/70e3b7de-c4d5-435f-98cd-91e49431946d)

![image](https://github.com/user-attachments/assets/81ff4052-f962-4822-9659-a4266a65e78f)

![image](https://github.com/user-attachments/assets/b0c6b1e8-f3e7-47e6-b9d8-1c5df7dd56c0)

![image](https://github.com/user-attachments/assets/92873fec-d698-43a7-a911-371dcfeb773d)

![image](https://github.com/user-attachments/assets/2272554a-3bc1-455d-99df-095426756366)



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
