# Ex-04-Multivariate-Analysis
# Aim
To perform Multivariate EDA on the given data set.

# Explanation
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

# Algorithm
# Step1
Import the built libraries required to perform EDA and outlier removal.

# Step2
Read the given csv file.

# Step3
Convert the file into a dataframe and get information of the data.

# Step4
Return the objects containing counts of unique values using (value_counts()).

# Step5
Plot the counts in the form of Histogram or Bar Graph.

# Step6
Use seaborn the bar graph comparison of data can be viewed.

# Step7
Find the pairwise correlation of all columns in the dataframe.corr()

# Step8
Save the final data set into the file.

# Code

Developed by : HARINI M D

Registration Number : 212222230043
```
import pandas as pd
import numpy as py
import seaborn as sns
import matplotlib.pyplot as plt

df=pd.read_csv('SuperStore.csv')
df
df.head()
df.info()
df.describe()
df.isnull().sum()
df.dtypes

sns.scatterplot(df['Postal Code'],df['Sales'],hue=df['Row ID'])

sns.barplot(x=df['Row ID'],y=df['Sales'],data=df)

states=df.loc[:,["State","Sales"]]
states=states.groupby(by=["State"]).sum().sort_values(by="Sales")
plt.figure(figsize=(17,7))
sns.barplot(x=states.index,y="Sales",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("STATES")
plt.ylabel=("SALES")
plt.show()

sns.barplot(df['Postal Code'],df['Ship Mode'],hue=df['Region'])

df.corr()
sns.heatmap(df.corr(),annot=True)
```
# Output

# Data
![image](https://user-images.githubusercontent.com/113497680/229694916-91c119bc-643f-4264-879f-5daa34ed4abc.png)
# Data head
![image](https://user-images.githubusercontent.com/113497680/229696960-a43fe45a-331c-4d76-aa74-3b00470f4d31.png)
# Data Information
![image](https://user-images.githubusercontent.com/113497680/229697059-211b409d-fcc2-4f64-876c-9e0fb9782f64.png)
# Data describe
![image](https://user-images.githubusercontent.com/113497680/229697270-1aea8849-7d60-40d0-b4d8-c6608f7ea7ab.png)
# Data Null Values
![image](https://user-images.githubusercontent.com/113497680/229697348-3fd1f4f9-fef6-430b-b36c-f77c3ab452c7.png)
# Data Types
![image](https://user-images.githubusercontent.com/113497680/229697432-705657bb-0919-4dd7-80a3-40e5f13a668b.png)
# Scatterplot
![image](https://user-images.githubusercontent.com/113497680/229697511-feafb5a0-412a-4ca0-852e-01071b097eea.png)
# Barplot
![image](https://user-images.githubusercontent.com/113497680/229697620-0ae10e83-5830-410a-a8f1-01db8ca6718a.png)
![image](https://user-images.githubusercontent.com/113497680/229697638-8a0ab4a3-fe5f-4970-8b5b-35aba9d9089e.png)
![image](https://user-images.githubusercontent.com/113497680/229697676-518cb510-1b63-4eae-8a60-650ea543c228.png)
# Correlation and Heatmap
![image](https://user-images.githubusercontent.com/113497680/229697755-8920a5b6-e816-42d8-938f-c055dadfa5d6.png)

![image](https://user-images.githubusercontent.com/113497680/229697793-1b43bd2e-2582-45c9-8828-aa38a86af81a.png)

# Result
Thus the program to perform EDA on the given data set is successfully executed.


