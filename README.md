# Ex-01_DS_Data_Cleansing


## AIM:
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation:
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM:
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE:
#For Data_set:
```
import pandas as pd
df=pd.read_csv("/content/Data_set(1).csv")
print(df)

df.head(5)

df.info()

df.isnull()

df.isnull().sum()

df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()

df.isnull().sum()
```
# For loan_data:
```
import pandas as pd
df=pd.read_csv("/content/Loan_Data(1).csv")
print(df)

df.head(5)

df.info()

df.isnull()

df.isnull().sum()

df['Loan_ID']=df['Loan_ID'].fillna(df['Education'].mode()[0])
df['Education']=df['Education'].fillna(df['Education'].mode()[0])
df['Married']=df['Married'].fillna(df['Education'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df.head()

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.head()

df.info()

df.isnull().sum()
```
### OUTPUT:
## For Data_set:
# Data
![Data](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/ba01b39f-48f8-4654-bbb5-911cb3af7b7e)
![Data2](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/5e843989-d3dc-4266-88d8-8a25e73016c7)


# NonNull before:
!![NONNULL 1](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/de91fe02-7ca2-47e4-913d-ec89d305dc44)
![NONNULL 2](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/5a55e8c5-b1d2-484a-9b26-f541f35eec69)
![NONNULL 3](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/4be8e142-a282-4506-b686-65e099d84f05)

# Mode:
![MODE](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/e9bc9d27-5134-460a-9c6f-b49142a69697)
# Mean:
![MEAN](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/c5d39504-78d9-490b-9a95-8b54cae1fa52)

# Median:
![MEDIAN](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/78bdf18e-1634-4a4e-a50a-c46bdbffc209)


# NonNull after:
![Nonnull af1](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/f53f31b6-41f3-48aa-8721-964162407b78)

![Nonnull af2](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/64e473ec-7e02-457e-8131-00c3e4c0938a)

### For loan_data:
# Data
![lndata](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/578921a2-bddb-49d1-8eec-f3d785203b74)
![lndata2](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/e8ed9ae7-b78b-4505-bdbc-05a1c6770987)
# NonNull before:
![lnnonnull1](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/2e6c58dc-5fd2-4699-b05c-1358aae9fb88)

![lnnonnull2](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/9351d518-92f3-4164-9042-ef761ac4a333)

# Mode:
![lnmode](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/f581b8d3-0460-468f-aa31-0ac56dc25fc7)
# Mean:
![lnmean](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/bce0be4b-3585-4ca6-8f69-0c66f8328807)

# Median:
![lnmedian](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/558e935d-3e5b-4a3f-a0a8-52991962201d)

# Nonnull after:

![lnnonullafter](https://github.com/abinayasangeetha/ODD2023-Datascience-Ex01/assets/119393675/f55a5f74-e473-49c0-8323-d77a003f478f)

## Result:
Thus the given data is read,cleansed and the cleaned data is saved into the file.
