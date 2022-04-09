# Ex-04-EDA
# AIM:
To perform EDA on the given data set.
# EXPLANATION:
The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
# ALGORITHM:
# STEP1:
Import the required packages(pandas,numpy,seaborn).
# STEP2:
Read the given .csv file.
# STEP3:
Convert the file into a dataframe and get information of the data.
# STEP4:
Remove the non numerical data columns using drop() method.
# STEP5:
Replace the null values using (.fillna).
# STEP6:
Returns object containing counts of unique values using (value_counts()).
# STEP7:
Plot the counts in the form of Histogram or Bar Graph.
# STEP8:
Find the pairwise correlation of all columns in the dataframe(.corr()).
# STEP9:
Save the final data set into the file.

# CODE:
~~~
PROGRAM DEVELOPED BY: R.SOMEASVAR.
REGISTER NUMBER: 212221230103.



import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("supermarket.csv")
df.info()
df.head()
df.tail()
df.isnull().sum()
df["City"].value_counts()
df["Gender"].value_counts()
df["Payment"].value_counts()
sns.countplot(x="Invoice ID",data=df)
sns.countplot(x="Total",data=df)
sns.countplot(x='gross income',data=df)
sns.countplot(x='Payment',data=df)
sns.displot(df["cogs"])
sns.countplot(x="Gender",hue="Quantity",data=df)
sns.displot(df[df["Product line"]==0]["Total"])
pd.crosstab(df["Payment"],df["Quantity"])
pd.crosstab(df["Gender"],df["Quantity"])
df.corr()
sns.heatmap(df.corr(),annot=True)
~~~

# OUTPUT:
# READ THE DATA:
![OUTPUT](./1.jpg)

![OUTPUT](./2.jpg)

![OUTPUT](./3.jpg)

# CHECKING THE MISSING VALUES IN THE DATASET :
![OUTPUT](./4.jpg)

# VALUE COUNTS :
![OUTPUT](./5.jpg)

![OUTPUT](./6.jpg)

![OUTPUT](./7.jpg)

# PLOTTING GRAPHS FOR VARIOUS DATASETS :
![OUTPUT](./8.jpg)

![OUTPUT](./9.jpg)

![OUTPUT](./10.jpg)

![OUTPUT](./11.jpg)

![OUTPUT](./12.jpg)

![OUTPUT](./13.jpg)

![OUTPUT](./14.jpg)

![OUTPUT](./15.jpg)

![OUTPUT](./16.jpg)

# CORRELATION :
![OUTPUT](./17.jpg)

# HEAT MAP:
![OUTPUT](./18.jpg)

# RESULT:
Thus the Exploratory Data Analysis (EDA) on the given data set is successfully completed.
