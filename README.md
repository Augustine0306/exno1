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
```python
import pandas as pd
df=pd.read_csv("/content/SAMPLEIDS.csv")
df
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/34e7e05b-0269-4ab9-95c7-2af342e14228)
```python
import pandas as pd
df=pd.read_csv('/content/SAMPLEIDS.csv')
print(df.info)
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/31d1d853-67bd-483c-a030-c10a1cfd9093)
```python
import pandas as pd
import pandas as pd
df=pd.read_csv('/content/SAMPLEIDS.csv')
print(df.head(13))
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/b1b043d7-f24e-4e4b-baa1-8a4d36c8e8f3)
```python
import pandas as pd
print(df.tail(12))
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/430923ea-9a22-40e4-96ee-abbc5b4dfb2d)
```python
import pandas as pd
print(df.describe)
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/3fb75bc6-d875-4ef4-9a82-934e5b0ca60c)
```python
df.isnull().sum()
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/8a93f553-cbaf-494d-a8ac-699e426673a0)
```python
df.nunique()
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/279ac593-00e7-48bf-9168-9374f7b87c50)
```python
df.TOTAL.fillna(mn,inplace=True)
df
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/338b6311-5835-4ea3-bff4-e5953fc777aa)
```python
min=df.M4.min()
min
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/b847c09d-b0ee-4c92-a231-5fed8dfe91a6)
```python
df.M4.fillna(min,inplace=True)
df
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/53f56f34-885a-4066-82e0-69c2851ec03a)

```python
import pandas as pd
import seaborn as sns
age=[1,3,28,27,25,92,30,39,40,50,26,24,29,94]
af=pd.DataFrame(age)
af
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/9c56d5f0-bc46-4d09-96e9-33d544370eb1)

```python
sns.boxplot(data=af)
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/b633d964-9cbd-452b-a726-d4ae315b9620)

```python
sns.scatterplot(data=af)
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/6ba75952-b609-453a-a788-d41fcd1a78b9)

```python
q1=af.quantile(0.25)
q2=af.quantile(0.50)
q3=af.quantile(0.75)
iqr=q3-q1
iqr
low=q1-1.5*iqr
low
high=q3+1.5*iqr
high
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/857b8d82-3d54-42f8-a32b-826a33e8c36a)

```python
af=af[((af>=low)&(af<=high))]
af
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/2f335749-2691-410c-93d1-cb14d4deb329)

```python
af.dropna()
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/e17a299a-8287-4b20-a2ef-1aa289949c93)

```python
sns.boxplot(data=af)
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/d14df7e9-025a-4300-b9e2-651c01feee9c)

```python
sns.scatterplot(data=af)
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/9b6ba307-6de5-4d61-aae5-a0d40fe1a533)

```python
data=[1,12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,72,75,78,81,84,87,90,93,96,99,102,105]
df=pd.DataFrame(data)
df
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/72e32fb0-8c14-4c62-bc7e-5f2f66c130d2)


```python
import numpy as np
from scipy import stats
z=np.abs(stats.zscore(df))
z
```
![image](https://github.com/Augustine0306/exno1/assets/119404460/65d28769-e8e8-4f0b-94c1-04e7958c625c)


## Result:
Thus the program for data cleaning using python has executed successfully.
