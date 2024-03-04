# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
## Data cleaning
### 1) Read and display DataFrame
```
import pandas as pd
df=pd.read_csv("/content/SAMPLEIDS.csv")
df
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/34e7e05b-0269-4ab9-95c7-2af342e14228)
### 2) Display head
```
df.head(4)
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/0179d83b-1c34-4c2c-9718-672b0b580ade)
### 3) Display tail
```
df.tail(4)
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/eb3af614-0f06-4b5c-ace5-fa39c4a622ed)
### 4) Info of datafram
```
df.info(3)
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/50d658d6-0c3a-4ece-865f-f24a9b52b268)
### 5) Describe about the dataframe
```
df.describe()
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/9d809cf9-2378-4638-9ba0-777d4dcdd06d)
### 6) Shape of the datafram
```
df.shape
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/1918648e-a437-4af8-94ba-d4d041b494ac)
### 7) Checking tha NUll values
```
df.isnull().sum()
```

![image](https://github.com/Augustine0306/exno1/assets/119404460/faa4ef4d-2f34-424a-8538-de56a0282ad4)
### 8) Drop the Null values
```
df.nunique()
```

![image](https://github.com/Augustine0306/exno1/assets/119404460/b6e775f4-751b-4950-a4c8-a186c5e2a030)
### 9) Finding the mean value
```
mn=df.TOTAL.mean()
mn
```

![image](https://github.com/Augustine0306/exno1/assets/119404460/19dafe4c-9b36-42d6-b088-3f1e6e384bd1)
### 10) Fill Null value with Mean value
```
df.TOTAL.fillna(mn,inplace=True)
df
```

![image](https://github.com/Augustine0306/exno1/assets/119404460/6a7baf07-59ac-475e-9397-bd69163b71c0)
### 11) Finding minimum value
```
mn=df.M4.min()
mn
```

![image](https://github.com/Augustine0306/exno1/assets/119404460/81fe521b-5c46-49eb-93c1-a5fe9c10627b)
### 12) Printing only Date of Birth
```
df['cd']=pd.to_datetime(df['DOB'])
df['cd']
```

![image](https://github.com/Augustine0306/exno1/assets/119404460/5cbf59e8-07cb-46f5-b8f3-dd2ec9e27d81)
## Result:
Thus the program for data cleaning using python has executed successfully.
