# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Ins# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required packages and print the present data.
2. Print the placement data and salary data.
3. Find the null and duplicate values.
4. Using logistic regression find the predicted values of accuracy , confusion matrices.

## Program & Output:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Mohamed Faizal M
RegisterNumber:  212223243002
*/
```
~~~
import pandas as pd
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, classification_report

data=pd.read_csv("/content/Placement_Data (1).csv") 
data.head()
~~~
![425912579-ca0f6616-e1c9-4474-b221-0542ad1fb076](https://github.com/user-attachments/assets/a346410d-aeec-49ac-aeed-d4bef2d58d1f)

~~~
data1=data.copy() 
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
~~~
![425912672-808a0582-0f2c-4b39-8fff-02639ebf1f44](https://github.com/user-attachments/assets/7b45405a-b62f-4c9a-abdb-e1bfb91a2f08)
~~~
data1.isnull()
~~~
![425912821-797771f6-a330-4ccc-94ef-4938ab863d99](https://github.com/user-attachments/assets/9b8451a5-d31d-4e56-b62e-46efb65d79ea)
~~~
data1.duplicated().sum()
~~~
![425913900-aa98c682-74eb-40be-99ce-cd1265a9dbe0](https://github.com/user-attachments/assets/30e31b3d-be9a-4108-a17b-b2f14f879ede)
~~~
le = LabelEncoder()
cols = ["gender", "ssc_b", "hsc_b", "hsc_s", "degree_t", "workex", "specialisation", "status"]
for col in cols:
    data1[col] = le.fit_transform(data1[col])
data1
~~~
![425913056-f502d7b6-d0c8-485a-98bc-1d78363df5f0](https://github.com/user-attachments/assets/f3642867-dad5-4c3a-ac62-095e94562b58)
~~~
x = data1.iloc[:, :-1]
x
y = data1["status"]
y
~~~
![425913144-96f6a06a-9411-4d52-99d2-3ec90168db93](https://github.com/user-attachments/assets/d687a1f2-6f73-48e5-b06e-d8abe5037ed9)
~~~
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=0)
lr = LogisticRegression(solver="liblinear")
lr.fit(x_train, y_train)
y_pred = lr.predict(x_test)
y_pred
~~~
![425913216-0fd052b3-68b5-429b-b889-21c49cdd943e](https://github.com/user-attachments/assets/8f99249a-7940-4d0b-a85c-477cf8504063)
~~~
accuracy = accuracy_score(y_test, y_pred)
print(accuracy)
~~~
![425913302-b00ae6d9-a3f0-43ff-82b5-8cc522f7b5b4](https://github.com/user-attachments/assets/45e7d2d5-1f15-47ce-9f86-576dab8adfb3)
~~~
classification_report1 = classification_report(y_test, y_pred)
print(classification_report1)
~~~
![425913371-51c516b6-fc76-48cc-8cdf-2ea80f0f013a](https://github.com/user-attachments/assets/2c2b98fa-bbd3-4439-823a-532a26610e89)
~~~
lr.predict([[1, 80, 1, 90, 1, 1, 90, 1, 0, 85, 1, 85]])
~~~
![425913437-3e42bfff-006b-42bb-91e5-8d965fd99daf](https://github.com/user-attachments/assets/fd562591-a3b3-41cc-9bd7-1fc086399fcd)



## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.tallation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: 
RegisterNumber:  
*/
```

## Output:
![the Logistic Regression Model to Predict the Placement Status of Student](sam.png)


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
