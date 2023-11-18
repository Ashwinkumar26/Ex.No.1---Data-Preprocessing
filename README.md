Ex.No.1---Data-Preprocessing
## AIM:
To perform Data preprocessing in a data set downloaded from Kaggle

## REQUIPMENTS REQUIRED:
Hardware – PCs Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:
Kaggle : Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

Data Preprocessing:

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis. Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

Need of Data Preprocessing :

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set. Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.

## ALGORITHM:
### STEP 1:
Importing the libraries

### STEP 2:
Importing the dataset

### STEP 3:
Taking care of missing data

### STEP 4:
Encoding categorical data

### STEP 5:
Normalizing the data

### STEP 6:
Splitting the data into test and train

### STEP 7:
End the program

## PROGRAM:
```
DEVELOPED BY:Ashwin Kumar K
REGISTER NO:212221223001
```
```
import pandas as pd

df=pd.read_csv("/content/Churn_Modelling.csv")

df.head()

df.isnull().sum()

df.drop(["RowNumber","Age","Gender","Geography","Surname"],inplace=True,axis=1)

print(df)

x=df.iloc[:,:-1].values

y=df.iloc[:,-1].values

print(x)

print(y)

from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()

df1 = pd.DataFrame(scaler.fit_transform(df))

print(df1)

from sklearn.model_selection import train_test_split

xtrain,ytrain,xtest,ytest=train_test_split(x,y,test_size=0.2,random_state=2)

print(xtrain)

print(len(xtrain))

print(xtest)

print(len(xtest))

from sklearn.preprocessing import StandardScaler

sc = StandardScaler()

df1 = sc.fit_transform(df)

print(df1)
```
## OUTPUT:
## OUTPUT :

### df.head() :

![Screenshot 2023-08-28 161148](https://github.com/Abrinnisha6/Ex.No.1---Data-Preprocessing/assets/118889454/0ea2d5d8-f985-4ba8-9390-b47ce4e2f8c2)

### df.isnull().sum() :

![Screenshot 2023-08-28 161229](https://github.com/Abrinnisha6/Ex.No.1---Data-Preprocessing/assets/118889454/2c4c7db6-fb1f-4feb-a7a7-3f50bc81710a)

### df value :

![Screenshot 2023-08-28 161407](https://github.com/Abrinnisha6/Ex.No.1---Data-Preprocessing/assets/118889454/dfa69f88-93fd-411a-a489-6f856f786c21)

### VALUES OF INPUT AND OUTPUT DATA ON VAR X AND Y :

![Screenshot 2023-08-28 161459](https://github.com/Abrinnisha6/Ex.No.1---Data-Preprocessing/assets/118889454/e479141c-f60c-44b8-8c0a-c0733e74670e)

![Screenshot 2023-08-28 161506](https://github.com/Abrinnisha6/Ex.No.1---Data-Preprocessing/assets/118889454/a32b1459-cbd3-44a9-a2e8-079f9f762a8f)


### NORMALIZING DATA:

![Screenshot 2023-08-28 161544](https://github.com/Abrinnisha6/Ex.No.1---Data-Preprocessing/assets/118889454/53188c26-e359-4cf8-aa1b-1df5073b35a1)
### X_TRAIN AND Y_TRAIN VALUES :

![Screenshot 2023-08-28 161638](https://github.com/Abrinnisha6/Ex.No.1---Data-Preprocessing/assets/118889454/73f46868-d029-4946-a929-7b93ef538ec2)


### X AND Y VALUES :

![Screenshot 2023-08-28 161715](https://github.com/Abrinnisha6/Ex.No.1---Data-Preprocessing/assets/118889454/4a85cb4d-40b2-4342-9949-7d1a35334ab6)

### X_TEST AND Y_TEST VALUES :

![Screenshot 2023-08-28 161751](https://github.com/Abrinnisha6/Ex.No.1---Data-Preprocessing/assets/118889454/8c23e0b3-b34e-4785-bdf5-89a7bbfa1a31)

RESULT:
Thus,the program to perform Data preprocessing in a data set downloaded from Kaggle is implemented successfully .
