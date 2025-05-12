# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

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
Program to implement the SVM For Spam Mail Detection..
Developed by: Ameen Basha A
RegisterNumber: 212224220008
*/
```
```
import chardet
file='/content/spam.csv'
with open(file,'rb') as rawdata:
  result=chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv('spam.csv',encoding='windows-1252')
data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.fit_transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```

## Output:
![image](https://github.com/user-attachments/assets/1a0a43ed-ec11-425b-8275-17504f873e1e)

![image](https://github.com/user-attachments/assets/d04deebc-df5c-4552-8d33-9529c83ed092)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
