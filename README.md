# Implementation of K-Means Clustering Algorithm
## Aim
To write a python program to implement K-Means Clustering Algorithm.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step1
Import the necessary packages.

### Step2
Read the csv file.

### Step3
Scatter plot the applicant income and loan amount.

### Step4
Obtain the kmean clustring for 2 classes.

### Step5
Pretict the cluster group of Applicant Income and Loanamount.

## Program:
```
Developed By: Jegathish s
Roll no: 21005410

import pandas as pd
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt
import seaborn as sns
x1=pd.read_csv("clustering.csv")
print(x1.head(2))
x2=x1.loc[:,["ApplicantIncome",'LoanAmount']]
print(x2.head(2))

x=x2.values
#print(x)
sns.scatterplot(x[:,0],x[:,1])
plt.xlabel("Income")
plt.ylabel('Loan')
plt.show()

Kmeans=KMeans(n_clusters=4)
kmeans.fit(x)
print("cluster centers:",kmeans.cluster_centers_)
print("Labes:",kmeans.labels_)
predict_class = kmeans.predict([[9000,1200]])
print("Cluster group for application income 9000 and loanamount 120 is",predict_class)
```
## Output:

### Insert your output

![output](o1.png)

## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.