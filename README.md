# Ex-09-Data-Visualization-

# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
## STEP 1
Read the given Data
## STEP 2
Clean the Data Set using Data Cleaning Process
## STEP 3
Apply Feature generation and selection techniques to all the features of the data set
## STEP 4
Apply data visualization techniques to identify the patterns of the data.



# CODE:
```
Developed By: SASIDEVI V
Register No: 212222230136
```

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
tips

tips.head()

tips.info()

# Which day of the week has the highest total bill amount?

sns.barplot(x='day',y='total_bill',data=tips)
plt.title("Weekly highest total bill amount")

# What is the average tip amount given by smokers and non-smokers?

sns.barplot(x='smoker',y='tip',data=tips, palette='rainbow')
plt.title("Average tip amount given by smokers and non-smokers")

# How does the tip percentage vary based on the size of the dining party?

sns.boxplot(x='size', y='tip',data=tips)
plt.title("Tip percentage based on the sizes of the dining party")

# Which gender tends to leave higher tips?

sns.boxplot(x='sex', y='tip',data=tips)
plt.title("Higher tips based on gender")

# Is there any relationship between the total bill amount and the day of the week?

plt.plot(tips['day'],tips['total_bill'])
plt.title("Relationship between the total bill amount and the day of the week")
plt.show()

# How does the distribution of total bill amounts vary across different time periods (lunch vs. dinner)?

sns.violinplot(x='time',y='total_bill',data=tips)
plt.title("Distribution of total bill amounts vary across different time periods(lunch vs. dinner)")

# Which dining party size group tends to have the highest average total bill amount?

sns.barplot(x='size',y='total_bill',data=tips)
plt.title("Highest average total bill amount based party size")

# What is the distribution of tip amounts for each day of the week?

sns.boxplot(x='day',y='total_bill',data=tips)
plt.title("Distribution of tip amounts for each day of the week")

# How does the tip amount vary based on the type of service (lunch vs. dinner)?

sns.violinplot(x='time',y='tip',data=tips)
plt.title("Tip based on the type of service ")

# Is there any correlation between the total bill amount and the tip amount?

sns.scatterplot(data=tips, x='total_bill', y='tip')
correlation_coefficient = tips['total_bill'].corr(tips['tip'])
print("Correlation Coefficient:", correlation_coefficient)
# heatmap
tips.corr()
plt.subplots(figsize=(7,5))
sns.heatmap(tips.corr(),annot=True)
```

# OUPUT
## DATASET
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/9aa3cb4d-174d-450e-b122-a096473dbe5a)

## tips.head()
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/57bf4842-7c04-412a-8e47-24a71530e9e6)

## tips.info()
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/2f0bf7e4-e88f-45b4-86ea-fec8884ddc7c)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/4e1695ab-6893-4106-8a3f-278dabfecc4e)


![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/1cbb8578-21ee-4e8b-a3ae-9492400e353c)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/b0c05d94-bf08-40c9-8fbd-85670eff33d8)


![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/dada071f-6fe1-476d-8e0d-856981a43701)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/11a3ff7d-22f5-43a5-9ba6-9e7aa5a733c9)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/96edbab2-cbe7-42b1-9094-c57ae0c28975)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/f01e6b7a-da3f-4252-a777-1873bb540951)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/36c15255-3e32-409d-a8b2-54c73a3bcf94)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/de7813c7-3eb7-4e7e-89b9-627b9931ad41)

![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/c3b2b883-4f9e-4d78-aaa7-484156737652)

## Heatmap
![image](https://github.com/SASIDEVIvenaram/Ex-08-Data-Visualization_1/assets/118707332/91696849-f049-4739-967a-52c6c272ae8d)

# RESULT:
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully based on tips dataset and the data is saved to file.
