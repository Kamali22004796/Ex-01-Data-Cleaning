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

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```
# OUPUT
# DATA

![Screenshot 2023-04-07 193413](https://user-images.githubusercontent.com/120567837/230622104-0c3d5927-d5af-465f-86bb-025edb9f1316.png)

![Screenshot 2023-04-07 193547](https://user-images.githubusercontent.com/120567837/230622292-63afd727-9447-467e-8835-5e06279a3004.png)

# NON NULL BEFORE

![Screenshot 2023-04-07 205217](https://user-images.githubusercontent.com/120567837/230640141-61f9d0b8-f020-4b6a-ae6f-bbba1a58fb49.png)

![Screenshot 2023-04-07 213500](https://user-images.githubusercontent.com/120567837/230640475-fa081f6b-4fb9-474d-afcc-97712056e10d.png)

![Screenshot 2023-04-07 213723](https://user-images.githubusercontent.com/120567837/230640835-6aac232e-e20d-497c-be94-ef7ed2560949.png)

# MODE

![Screenshot 2023-04-07 213930](https://user-images.githubusercontent.com/120567837/230641136-b819951b-0188-4fd4-af36-d7c22b74e5e6.png)

# MEAN

![Screenshot 2023-04-07 214229](https://user-images.githubusercontent.com/120567837/230641552-737d9fdb-0387-4fe6-8410-0cc094bccb28.png)

# MEDIAN

![Screenshot 2023-04-07 214427](https://user-images.githubusercontent.com/120567837/230641834-5ee89c8d-fbb1-4284-a94f-d94dbdf281b9.png)

# NON NULL AFTER

![Screenshot 2023-04-07 214605](https://user-images.githubusercontent.com/120567837/230642095-856dc5b4-4a83-4f70-8a5d-70fa0d6b4567.png)

![Screenshot 2023-04-07 215034](https://user-images.githubusercontent.com/120567837/230642765-5f36c8c6-0c2a-4f3b-b95a-0b96aedf5709.png)

# RESULT
Thus, the given data is read, cleansed and the cleansed data is saved into the file.
