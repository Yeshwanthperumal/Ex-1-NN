<H3>ENTER YOUR NAME: YESHWANTH P</H3>
<H3>ENTER YOUR REGISTER NO. 212222230178</H3>
<H3>EX. NO.1</H3>
<H3>DATE</H3>
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

### Importing the necessary libraries
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
```

### Read the dataset
```
df=pd.read_csv("Churn_Modelling.csv",index_col="RowNumber")         
df.head()
```

### Finding the missing values
```
df.isnull().sum()
```

### Checking for duplicates
```
df.duplicated().sum()
```

### Detect the outliers
```
df=df.drop(['Surname', 'Geography','Gender'], axis=1)
```

### Normalize the Data Set
```
scaler=StandardScaler()                                             
df=pd.DataFrame(scaler.fit_transform(df))
df.head()
```

### Split the data into input and output
```
X,Y=df.iloc[:,:-1].values ,df.iloc[:,-1].values                     
print('Input:\n',X,'\nOutput:\n',Y)
```

### Split the data for training & testing
```
Xtrain,Xtest,Ytrain,Ytest = train_test_split(X, Y, test_size=0.2)
```

### Printing the training data and test data
```
print("Xtrain:\n" ,Xtrain, "\nXtest:\n", Xtest)                     
print("\nYtrain:\n" ,Ytrain, "\nYtest:\n", Ytest)
```

## OUTPUT:

### DATASET
![image](https://github.com/user-attachments/assets/316e73f8-3f95-4217-9041-7c05cc575496)

### NULL VALUES
![image](https://github.com/user-attachments/assets/b85847c9-80a4-4964-9409-ae44f4db0406)

### NORMALIZED DATA
![image](https://github.com/user-attachments/assets/31c06b6c-f5bd-446a-8364-c2ea16d3f758)

### DATA SPLITING
![image](https://github.com/user-attachments/assets/cde056f3-6e70-4308-808c-a7aab9fdb0f1)

### TRAIN AND TEST DATA
![image](https://github.com/user-attachments/assets/318c0448-eeee-41bd-bddd-3c9550b9a717)

## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


