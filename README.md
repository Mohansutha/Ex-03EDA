# Ex-03EDA

## AIM
To perform EDA on the given data set. 

# Explanation
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 

# ALGORITHM
### STEP 1
Read the given Data

### STEP 2
Get the information about the data

### STEP 3
Remove the null values from the data

### STEP 4
Save the Clean data to the file




# CODE
~~~
import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head()
df.tail()
df.isnull().sum()
df.drop("Cabin",axis=1,inplace=True)
df.info()
df.isnull().sum()
df["Age"]=df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull().sum()
df["Embarked"]=df["Embarked"].fillna(df["Embarked"].mode()[0])
df.isnull().sum()
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
sns.countplot(x="Survived",data=df)
sns.countplot(x="Pclass",data=df)
sns.countplot(x="Sex",data=df)
df.info()
sns.displot(df["Fare"])
sns.countplot(x="Pclass",hue="Survived",data=df)
sns.displot(df[df["Survived"]==0]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Sex"],df["Survived"])
df.corr()
sns.heatmap(df.corr(),annot=True)
~~~
# OUPUT

![id 1](https://user-images.githubusercontent.com/94828335/167985174-033bb752-a5ba-4920-b117-d2c0ecb19d64.png)

![id 2](https://user-images.githubusercontent.com/94828335/167985227-ef7c70c2-b7d3-4897-8918-0d47adae70aa.jpg)

![id 3](https://user-images.githubusercontent.com/94828335/167985272-dafe8e2d-c42c-4c86-9b2c-fe73868c6342.jpg)

![id4](https://user-images.githubusercontent.com/94828335/167985295-43bc06ad-8f2a-4d48-8b7e-be7b61e8de18.png)

![id 5](https://user-images.githubusercontent.com/94828335/167985320-cccbf353-e878-4619-b49e-b23aaa75a50e.png)

![id6](https://user-images.githubusercontent.com/94828335/167985355-1b79c377-0d4b-4738-9305-72266b5dc5fb.jpg)

![id 7](https://user-images.githubusercontent.com/94828335/167985386-e03d2ab2-2a6a-4ef2-b5e6-59f03ccfba7a.jpg)

![id 8](https://user-images.githubusercontent.com/94828335/167985420-7d11ea23-9d42-4e06-afe9-ca03ec11ef85.jpg)

![id 9](https://user-images.githubusercontent.com/94828335/167985445-3b045a91-d5b0-450f-b3ac-8c171f192ea7.jpg)

![id10](https://user-images.githubusercontent.com/94828335/167985480-22e78fea-fcb2-472b-80ed-ef8f5eb28821.jpg)

![id11](https://user-images.githubusercontent.com/94828335/167985495-7b02e26b-28eb-4dce-a157-b654347debce.jpg)

![id12](https://user-images.githubusercontent.com/94828335/167985527-9a8b8d54-3099-46c2-b1ef-90490346c848.jpg)

![id13](https://user-images.githubusercontent.com/94828335/167985550-5c45bd2b-30d0-400b-9122-65f5b6905a4d.jpg)

![id 14](https://user-images.githubusercontent.com/94828335/167985572-13bacf66-b839-43dd-9ac0-602e25794930.jpg)

![id15](https://user-images.githubusercontent.com/94828335/167985589-17a869e9-d909-4898-a05b-b9a8e13c0c66.jpg)



### Result 

Thus the EDA on the given data set is sucessfully done.















