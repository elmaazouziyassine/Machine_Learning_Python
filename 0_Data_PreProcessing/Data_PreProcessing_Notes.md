# Data PreProcessing
### **Step 1 : Import libraries**

| Library        | Import Syntax           | Purpose  |
|:-------------|:-------------|:-----|
|Numpy|`import numpy as np`|to ...|
||`import pandas as pd`||
||`import matplotlib.pyplot as plt`||
||`import seaborn as sns`||
||`import sklearn`||
||`%matplotlib inline`||

### **Step 2 : Import Datasets**
`myData = pd.read_csv('path/myFile.csv', sep=',')` \
`myData.head`

### **Step 3 : Explore Data**
##### ***Understand Categorical Data***
##### ***Understand Numerical Data***


### **Step 5 : Handle missing numerical values**


Data can have missing values due to a number of reasons such as :

Observations not recorded
Data corruption
Hadnling missing values is important as many machine learning algorithms do not support data with missing values.

Objectives :

How to mark invalid or corrupt values as missing in the dataset.
How to remove rows with missing data from the dataset.
How to impute missing values with mean values in the dataset.
Various techniques to handle missing values :

Delete the records with a at least one missing value.
Create a sperate model to handle a missing values.
Use statistical methods (mean, median or mode,...)
Best technique to handle missing values
How ? :
- Create a heatmap to detect missing values : \
`myData.isnull()` or
`sns.heatmap(myData.isnull(), yticklabels=False, cbar=False, cmap='viridis')`

**First Approach : Delete the records with at least one missing value.**
- Use this apprach in case of use of a huge data set (milions of records).

**Second Approach : Create a seperate model to handle missing values.**
- Suppose a dataset with : f1, f2, f3, f4, targetVariable. 
- suppose only the feature variable f1 contains some missing values. 
- create a model with features: f2, f3, f4 and target = f1 
- train the model and get the mising values
Consider the record with at least one 

Do this steps for all the variables with missing values.
missing value in the Test Set.
- Drawbacks : need much more time : Computational effort

**Third & Best Approche : Replace the missing values by some statistical values (such as : mean, median, mode1,...).**

- Mean = average (sum of values/number of values)
- Median = sort values and  then take the median one.
- Mode 1 = high frequency value 



- **Step 6 : Encode categorical data**
2 types of Categorical Data : 
- Categorical Data which values are the same importance : countries 
- Categorical Data which values are with different importance : low, medim, high

Attention Point : For the first type, we have to prevent maching learning algorithms to think that for example Germany is greather than France or Spain.

### **Step 4 : Separate Features Variables from Target Variable**
- Feature Variables has to be stored in a MATRIX
- Target Variable has to be stored in a VECTOR

7. Feature Scaling.
**Objective** : Put the Numerical Data at the same scale. For example : values between -1 to 1.
The columns "age" and "Salary" dont have the same scale. This will cause some issues in some machine learning algorithms because a lot of models are bases in the Euclidean Distance.  (Here, the salary will dominate the distance. The age will be neglected.) 

8. Split Dataset into Training Set and Test Set. 
