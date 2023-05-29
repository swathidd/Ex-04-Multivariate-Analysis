# Ex-04-Multivariate-Analysis
# AIM:
To do multivariate analysis on the given data

## EXPLANATION:
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

# ALGORITHM:

STEP 1:

Import the built libraries required to perform EDA and outlier removal.

STEP 2:

Read the given csv file.

STEP 3:

Convert the file into a dataframe and get information of the data.

STEP 4:

Return the objects containing counts of unique values using (value_counts()).

STEP 5:

Plot the counts in the form of Histogram or Bar Graph.

STEP 6:

Use seaborn the bar graph comparison of data can be viewed.

STEP 7:

Find the pairwise correlation of all columns in the dataframe.corr() .

STEP 8:

Save the final data set into the file.
## POROGRAM
```
import pandas as pd

df=pd.read_csv('/content/SuperStore.csv')

df.head()

df.dtypes

df.corr()

import seaborn as sns

sns.heatmap(df.corr(),annot=True)

import matplotlib.pyplot as plt

states=df.loc[:,["State","Postal Code"]]

states=states.groupby(by=["State"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(10,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("STATE")

plt.ylabel=("POSTAL CODE")

plt.show()
```

# OUTPUT:
# DATASET

![image](https://user-images.githubusercontent.com/121300272/230836981-b01cf8c5-f270-42b8-a8b0-416d4961ba0e.png)

# HEAD()
![image](https://user-images.githubusercontent.com/121300272/230837193-ef2a8d36-a975-4a4e-8caa-87ac7589d826.png)

# INFO()
![image](https://user-images.githubusercontent.com/121300272/230837297-5bb9f79e-7425-443d-9151-89e5528c43e3.png)

# DESCRIBE()
![image](https://user-images.githubusercontent.com/121300272/230837418-607aa1ef-a64b-478f-885e-ce7ce763d734.png)

# DATATYPE()
![image](https://user-images.githubusercontent.com/121300272/230837535-f231000a-000c-407f-af6e-5008b6f26969.png)

# ISNULL()
 ![image](https://user-images.githubusercontent.com/121300272/230837659-2a46f425-672d-4301-b106-9a3aae82e478.png)
 
# Postal code has outliers.
![image](https://user-images.githubusercontent.com/121300272/230837794-b7c52ee1-3ae2-4c61-bbf8-48904b8b680e.png)

# After removing outliers from Postal Code.

# MULTIVARIATE ANALYSIS

# SCATTER PLOT
![image](https://user-images.githubusercontent.com/121300272/230837943-1faa65ba-c1d1-4925-a63a-2cc2ca21bbeb.png)

# BARPLOT
![image](https://user-images.githubusercontent.com/121300272/230838094-010f24f1-9a74-46f0-b661-f40b1983a4c2.png)

![image](https://user-images.githubusercontent.com/121300272/230838227-b0313c44-7458-4165-ac26-3f4d5a70f426.png)

![image](https://user-images.githubusercontent.com/121300272/230838363-c57ed090-c242-4d20-8075-bd302b71804d.png)


# SEGMENTATION
![image](https://user-images.githubusercontent.com/121300272/230838519-d8ff94ba-caf0-43d5-b5e0-18a05afecff7.png)

# CORRESSION
![image](https://user-images.githubusercontent.com/121300272/230838722-0278993b-4492-447e-a259-89554b4b15ab.png)
 
 # HEATMAP()
 ![image](https://user-images.githubusercontent.com/121300272/230838886-8bc05df0-7bcb-44c3-8745-132ce04bd478.png)


# RESULT
Hence The Performance of the Multivariate EDA on the given data set is verified.

