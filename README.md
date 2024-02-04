# Titanic dataset
## Table of contents 
- [ Overview](#overview)
- [Aim](#aim)
- [Data Source](#data-source)
- [Tools Used](#tools-used)
- [Data Cleaning](#data-cleaning)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [Recommendations](#recommendations)
### Overview
This analysis focus on identifying the key features that contribute to survival rate of passengers and by  feature selection and analysis recommendation were provided.
![ATMpyCharts](https://github.com/Abiatm/Titanic_dataset/assets/153201833/9aa9991e-d730-4d96-9bac-1375fa50d4f6)

![Pynlargest](https://github.com/Abiatm/Titanic_dataset/assets/153201833/14522a2d-7934-4e99-9084-2f188998ec44)
### Aim
This work aim at visualizing various survival possibilities with respects to different features.

### Data Source
The dataset used for this analysis is the from Kaggle
[Download here]( https://www.kaggle.com/c/titanic/data?select=train.csv)
### Tools Used
- Python(Jupyter_Notebook) - Data cleaning,Data munging, Data visualization
- PowerBi- visualization validation
- Excel- Data cleaning validation
### Data Cleaning
 #### List of things checked and evaluated are:
 - Trimming of data
 - Removal of duplicates
 
 - Adding new column (eg Family_size column,Title column)
- Filtering and droping of column with high percentage of null values
- Filling of null values where necessary
- cleaning operation
 ### Data Analysis
```Python
import numpy as np
import pandas as pd
import matplotlib.pyplot  as plt
import seaborn as sns
%matplotlib inline
df_train["Family_size"] = 1 +  df_train['SibSp'] + df_train['Parch']
A=df_train["Name"].str.split(pat=",",expand=True)[1].str.split(pat=".",expand=True)
A[0]
A["Title"] =A[0]
df_N = pd.concat([df_train,A["Title"]],axis ="columns")
df_N["Age"].fillna(df_N["Age"].median(),inplace =True)
DA=df_N

fig = plt.figure(figsize=(15,10))


plt.subplots_adjust(wspace=0.15)
plt.style.use("seaborn-white")

fig.add_subplot(2, 2, 1)

sns.countplot(x= DA["Pclass"],hue =DA["Survived"],data=DA,edgecolor='black', linewidth=1,palette='PuBu')

fig.add_subplot(2, 2, 2)
sns.countplot(x= DA["Sex"],hue="Survived",data=DA,edgecolor='black', linewidth=1,palette='PuBu',width =0.8)

fig.add_subplot(2, 2, 3)
sns.countplot(x= DA["Embarked"],data=DA,edgecolor='black', linewidth=1,palette='BrBG')



fig.add_subplot(2, 2, 4)

sns.countplot(x= DA["Pclass"],hue =DA["Sex"],data=DA,edgecolor='black', linewidth=1,palette='GnBu')




plt.show()
```
### Results
The results from my observation shows:
1.	From the obtained visualization it shows that females survived more than males
2.	The higher the class or influence of a passenger the higher survival possibility
3.	There is high death rate than survival rate from the survived count.

### Recommendations
The following recommendations are made to prevent future loss:
1.	Due to possibility of implementation of women and children first rule while male comes last thereby leading to great loss of life,I recommend that it should be by checking some factors such as medical needs ,ability to rescue oneself or others and physical fitness.
2.	By ensuring fair access to resources, survival skills and capabilities it will help to save the classes of people in the ship
3.	More provisions is needed such as lifeboat, fire-resistant materials, better communication with passengers and more safety devices so as prevent loss of lives.
