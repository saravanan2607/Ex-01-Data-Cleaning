# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

## Program:
```
/* 
Name : C Saravanan
Register Number : 21222110041
**Data Cleaning - Data_set.csv**
import numpy as np
import pandas as pd
import seaborn as sbn
df = pd.read_csv("/content/Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name'] = df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on'] = df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network'] = df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
df['rating'] = df['rating'].fillna(df['rating'].mean())
df['current_overall_rank'] = df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers'] = df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()

**Data Cleannig - Loan_data.csv**
data = pd.read_csv("/content/Loan_data.csv")
print(data)
data.head(5)
data.isnull()
data.isnull().sum()
data['Gender'] = data["Gender"].fillna(data['Gender'].mode()[0])
data['Dependents'] = data["Dependents"].fillna(data['Dependents'].mode()[0])
data['Self_Employed'] = data["Self_Employed"].fillna(data['Self_Employed'].mode()[0])
data['Credit_History'] = data["Credit_History"].fillna(data['Credit_History'].mode()[0])
data.head()
data['LoanAmount']=data['LoanAmount'].fillna(data['LoanAmount'].median())
data.head()
data['Loan_Amount_Term']=data['Loan_Amount_Term'].fillna(data['Loan_Amount_Term'].mean())
data.head()
data.info()
data.isnull().sum()
*/
```


## OUPUT:
## Data Cleaning - Data_set.csv
![data set 1](https://user-images.githubusercontent.com/127843136/227728768-bbccf434-e25c-4aa9-ba7e-7596c26adef4.png)

## Before Cleaning
![Data set 2](https://user-images.githubusercontent.com/127843136/227729073-8d51b114-e4b9-4bed-a981-4e977424b7ca.png)
![Data set 3](https://user-images.githubusercontent.com/127843136/227728980-00e240b9-e061-456e-a710-d641a9f04104.png)
![data set 4](https://user-images.githubusercontent.com/127843136/227729047-72f38e74-bdf2-4268-9c71-de0bd27fcd8c.png)

## Mode
![Mode](https://user-images.githubusercontent.com/127843136/227729179-e63080d0-7d3b-49df-ad91-e11f96f5d186.png)

## Mean
![Mean](https://user-images.githubusercontent.com/127843136/227729192-17362c03-cefa-49fd-bf87-adb568cb711d.png)

## Median
![Median](https://user-images.githubusercontent.com/127843136/227729199-778aaa9e-3be6-4a50-9fda-ff4ff09ce825.png)

## After Cleaning
![After Cleaning Data set](https://user-images.githubusercontent.com/127843136/227729205-f0fbcd0d-a399-4c63-8e6b-a38d77785987.png)

## Data Cleaning - Loan_data.csv

![Loan data 1](https://user-images.githubusercontent.com/127843136/227729245-a3c6fd03-1fa8-42cf-80a0-30e56a790b78.png)

## Before Cleaning
![Loan data 3](https://user-images.githubusercontent.com/127843136/227729261-ab45868e-a37d-4327-9cab-de461d253df8.png)
![Loan data 4](https://user-images.githubusercontent.com/127843136/227729265-af7ab162-8da6-41c5-83f8-8f44ac3ed842.png)
![Loan data 5](https://user-images.githubusercontent.com/127843136/227729285-cd3afccd-660a-41b2-addc-a7c41b590ab9.png)

## Mode
![Loan data Mode](https://user-images.githubusercontent.com/127843136/227729529-8674063c-af7b-4a8e-8c21-37faa7913458.png)

## Mean
![Loan data Mean](https://user-images.githubusercontent.com/127843136/227729536-eb122938-efc7-4a22-88b5-45fa4bc8fa3b.png)

## Median
![Medain Loan Data](https://user-images.githubusercontent.com/127843136/227729542-4b732463-83f0-4b1b-96c7-ea4c8436136c.png)

## After Cleaning
![Loan data 8](https://user-images.githubusercontent.com/127843136/227729553-a3b52952-3d18-49ad-b879-61c893a5e738.png)

# RESULT
Thus the given data is read, cleansed and the cleaned data is saved into the file.





