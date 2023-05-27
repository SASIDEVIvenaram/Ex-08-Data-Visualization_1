# Ex-09-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE:
```
Developed by: SASIDEVI V ,
Register No.: 212222230136
```
```
import pandas as pd
import seaborn as sns
from matplotlib import pyplot as plt
df=pd.read_csv("/content/Superstore - Superstore.csv (1).csv")

df.head()

df.info()

df.isnull().sum()

# Data Visualization using seaborn
# lineplot
sns.lineplot(x="Category",y="Sales",data=df,marker='o')

sns.lineplot(x='Ship Mode', y='Category',hue="Segment",data=df)
plt.title("Multiline Plot")
plt.show()

# barplot
sns.barplot(x="Category",y="Sales",data=df)

sns.barplot(x='Region', y='Sales', data=df,palette='Set1')
plt.title("Sales in different Regions")
plt.show()

# scatterplot
sns.scatterplot(x='Category',y='Sub-Category',data=df)
plt.title("Scatterplot")
plt.show()

sns.scatterplot(x='Category',y='Sub-Category',hue='Segment',data=df)
plt.show()

# boxplot
sns.boxplot(x="Sub-Category",y="Discount",data=df)
plt.xticks(rotation=90)

sns.boxplot( x="Profit", y="Category",data=df)

# pointplot
sns.pointplot(x=df["Quantity"],y=df["Discount"])

# violinplot
sns.violinplot(x="Profit",data=df)

# countplot
sns.countplot(x="Category",data=df)

sns.countplot(x="Sub-Category",data=df)
plt.xticks(rotation=90)
 
# histogram
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')

# KDEplot
sns.kdeplot(x="Discount", data = df,hue='Category')


# Data Visualization using Matplotlib

# plot
plt.plot(df['Region'], df['Sales'])
plt.show()

# Heatmap
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)

# piechart

df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()

# Histogram
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="black",bins=10)
plt.xticks(rotation =90)
plt.show()

# barplot
plt.bar(df['Category'],df.index)
plt.show()

# scatterplot
plt.scatter(df["Region"],df["Profit"], c ="red")
plt.show() 
 
# boxplot
plt.boxplot(x="Sales",data=df)
plt.show()

```

# OUPUT
## df.head()
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/e013412e-079f-4614-ab1c-0bee072353c4)

## df.info()
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/f03386ab-8152-4202-a152-3f6ff73fafe3)


## df.isnull().sum()
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/19ba2a91-af41-4a0c-986f-7158c4036529)


## Data Visualization using seaborn
### 1.LinePlot
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/c6a5cad9-6d63-4b2c-9583-505226f21d61)
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/2f57a08e-c9cc-4ac2-be59-98739061f859)


### 2.Barplot
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/83717137-f763-4fd7-9b52-809fe72d3b8c)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/467455a5-7d21-4c4c-94e5-d77c69fb848d)


### 3.ScatterPlot
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/ff6ce96a-cf00-4123-a744-a87aa24e7a46)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/fac1e83e-8d3b-478b-a739-fd66d75a93aa)


### 4.BoxPLot
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/3ee2d97e-6fcb-432f-9330-bfa9a27e8639)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/a94b5771-5bd3-48aa-b2ad-f80935f0bdb5)



### 5.PointPlot
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/691b5757-44a2-4a49-97e9-4df36ed55a1d)

### 6.ViolinPlot

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/59664c73-a12c-4982-9dd9-4eec59f89a1f)

### 7.CountPlot
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/1147dd75-e5fd-46b9-a540-0627a84f0a6b)

### 8.Histogram
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/47349284-7356-462b-ac2e-9126550a2aaf)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/82268972-c2d7-42e3-bf25-15df8698c6ab)

### 9.KDE Plot

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/5f64a337-fa64-45f3-9ba0-7e51e26c95c1)

## Data Visualization using Matplotlib

### 1.Plot
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/9829544b-477c-486a-8a37-d40be799d42d)


### 2.Heatmap
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/081445fe-2193-4dc8-a64b-66ac90f7f282)

### 3.Piechart
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/93bc2e57-2981-499d-a1ef-82ea7afd4606)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/6a0b70cc-8c41-4ec1-91f8-824d53a46191)

### 4.Histogram

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/4a1aadf3-763d-495e-8717-bd5a2f5b1c4e)

### 5.Barplot
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/a2f21c65-8f89-418f-bcb4-b195d38ca339)

### 6.ScatterPlot

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/fd4c08d7-8cd8-43cc-8bb8-bd7467fd16aa)

### 7.Boxplot

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization-/assets/118707332/d7a0e9a4-54bf-4426-8fc1-23523c5f5058)


# Result :
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.

