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


### Aim
This work aim at visualizing various survival possibilities with respects to different features.

### Data Source
The dataset used for this analysis is the from Kaggle
[Download here]( https://www.kaggle.com/c/titanic/data?select=train.csv)
### Tools Used
- Python(Jupyter  Notebook) - Data cleaning,Data munging, Data visualization
- PowerBi- visualization validation
- Excel- Data cleaning validation
### Data Cleaning
 #### List of things checked and evaluated are:
 - Trimming of data
 - Removal of duplicates
 - Converting text to columns
- Adding new column (eg Family_size column,Title column)
 - Filtering and droping of column with high percentage of null values
  -Filling of null values where necessary
- cleaning operation
 ### Data Analysis
```SQL
1	SELECT sum(total_price)  as Total_Revenue FROM spizza.`pizza_sales_excel_file - copy`;
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
