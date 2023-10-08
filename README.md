# EX-05-Feature-Generation
## AIM:
To read the given data and perform Feature Generation process and save the data to a file.

## EXPLANATION:
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

## ALGORITHM:
### STEP 1
Read the given Data

### STEP 2
Clean the Data Set using Data Cleaning Process

### STEP 3
Apply Feature Generation techniques to all the feature of the data set

### STEP 4
Save the data to the file

## PROGRAM & OUTPUT:
```
import pandas as pd
from scipy import stats
import numpy as np
df=pd.read_csv("/content/bmi.csv")
from sklearn.preprocessing import StandardScaler
sc=StandardScaler()
df[['Height','Weight']]=sc.fit_transform(df[['Height','Weight']])
df.head(10)
```
![image](https://github.com/Sanjay-sg/ODD2023-Datascience-Ex-05/assets/119559022/7fbd5d00-ea0a-46b2-a594-af13e45d075e)

```
import pandas as pd
df=pd.read_csv("/content/Encoding Data (1).csv")

from sklearn.preprocessing import LabelEncoder,OrdinalEncoder

temp=["Cold","Warm","Hot"]

enc=OrdinalEncoder(categories=[temp])

df["ord_2"]=enc.fit_transform(df[["ord_2"]])
df
```
![image](https://github.com/Sanjay-sg/ODD2023-Datascience-Ex-05/assets/119559022/194b6e1a-16cd-4175-b8f2-36a4916c8984)

```
from sklearn.preprocessing import OneHotEncoder

ohe=OneHotEncoder(sparse=False)
ohe.fit_transform(df[["nom_0"]])
```
![image](https://github.com/Sanjay-sg/ODD2023-Datascience-Ex-05/assets/119559022/26b9294b-e225-4c27-99b2-195330ca9821)

```
df=pd.read_csv("/content/bmi(1).csv")

from sklearn.preprocessing import MinMaxScaler
mms=MinMaxScaler()
df=pd.DataFrame(mms.fit_transform(df),columns=['Height','Weight','Index'])
df
```
![image](https://github.com/Sanjay-sg/ODD2023-Datascience-Ex-05/assets/119559022/f08a9148-9365-4ce5-b1b9-ab72c9005c44)

```
from sklearn.preprocessing import MaxAbsScaler
mas=MaxAbsScaler()
df=pd.DataFrame(mas.fit_transform(df),columns=['Height','Weight','Index'])
df
```
![image](https://github.com/Sanjay-sg/ODD2023-Datascience-Ex-05/assets/119559022/c2235c0c-36ba-4bd1-ad0c-5f9205ec4ff8)

```
from sklearn.preprocessing import RobustScaler
rs=RobustScaler()
df=pd.DataFrame(rs.fit_transform(df),columns=['Height','Weight','Index'])
df
```
![image](https://github.com/Sanjay-sg/ODD2023-Datascience-Ex-05/assets/119559022/993e678f-058b-445b-844e-a812254c52a4)

## RESULT:
Feature Generation process and Feature Scaling process is applied to the given data frames sucessfully.

