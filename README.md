<H3>ENTER YOUR NAME</H3> S V SHADHANASHREE
<H3>ENTER YOUR REGISTER NO.</H3> 212223230202
<H3>EX. NO.1</H3>
<H3>DATE</H3> 07.03.2025
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:

### Import Libraries
```
from google.colab import files
import pandas as pd
import seaborn as sns
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
from scipy import stats
import numpy as np
```
### Read the dataset
```
df=pd.read_csv("Churn_Modelling.csv")
```
### Checking Data

```
df.head()
df.tail()
df.columns
```
### Check the missing data
```
df.isnull().sum()
```

### Check for Duplicates
```
df.duplicated()
```
### Assigning Y
```
y = df.iloc[:, -1].values
print(y)
```
### Check for duplicates
```
py df.duplicated()
```

### Check for outliers
```
df.describe()
```
### Dropping string values data from dataset
```
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
```
### Checking datasets after dropping string values data from dataset
```
data.head()
```
### Normalize the dataset
```
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```
### Split the dataset
```
X=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(X)
print(y)
```
### Training and testing model
```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```


## OUTPUT:

### Data checking
![Screenshot 2025-03-07 114240](https://github.com/user-attachments/assets/15f9af78-e761-46b9-838f-63d71a59f26c)

### Missing Data

![Screenshot 2025-03-07 114815](https://github.com/user-attachments/assets/5063d338-d3db-4eb7-ba4e-d0aec325de50)


### Duplicates identification

![Screenshot 2025-03-07 114253](https://github.com/user-attachments/assets/c4ae9d6d-1d86-4561-b51e-83a998db9641)

### Values of 'Y'

![Screenshot 2025-03-07 114302](https://github.com/user-attachments/assets/1f5b7999-ea03-466e-98d3-3c6634cdab39)

### Outliers

![Screenshot 2025-03-07 114323](https://github.com/user-attachments/assets/f1891045-b594-4676-965f-570098855309)

### Checking datasets after dropping string values data from dataset

![Screenshot 2025-03-07 114343](https://github.com/user-attachments/assets/69fcf6c4-01cd-4bb3-be40-3cc060480468)

### Normalize the dataset

![Screenshot 2025-03-07 114355](https://github.com/user-attachments/assets/a8352de2-daa4-48e0-adf0-74ab95ad2caf)

### Split the dataset

![Screenshot 2025-03-07 114408](https://github.com/user-attachments/assets/9053676c-8b90-4374-9d77-ee3c36fa7cfb)

### Training and testing model


![Screenshot 2025-03-07 114421](https://github.com/user-attachments/assets/62be2111-f56b-4b3c-8352-278b617c33ed)









## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


