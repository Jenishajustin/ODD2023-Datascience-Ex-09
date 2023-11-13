# Ex:09 Data Visualization

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

## EXPLANATION
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
1. Read the given Data
2. Clean the Data Set using Data Cleaning Process
3. Apply Feature generation and selection techniques to all the features of the data set
4. Apply data visualization techniques to identify the patterns of the data.


## CODE
```
Name: JENISHA.J
Reg.No: 212222230056
```
```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset('tips')
tips

tips.head()

tips.info()
```
#### Which day of the week has the highest total bill amount?
```
sns.barplot(x='day',y='total_bill',data=tips)
plt.title("Weekly highest total bill amount")
```
#### What is the average tip amount given by smokers and non-smokers?
```
sns.barplot(x='smoker',y='tip',data=tips, palette='rainbow')
plt.title("Average tip amount given by smokers and non-smokers")
```
#### How does the tip percentage vary based on the size of the dining party?
```
sns.boxplot(x='size', y='tip',data=tips)
plt.title("Tip percentage based on the sizes of the dining party")
```
#### Which gender tends to leave higher tips?
```
sns.boxplot(x='sex', y='tip',data=tips)
plt.title("Higher tips based on gender")
```
#### Is there any relationship between the total bill amount and the day of the week?
```
plt.plot(tips['day'],tips['total_bill'])
plt.title("Relationship between the total bill amount and the day of the week")
plt.show()
```
#### How does the distribution of total bill amounts vary across different time periods (lunch vs. dinner)?
```
sns.violinplot(x='time',y='total_bill',data=tips)
plt.title("Distribution of total bill amounts vary across different time periods(lunch vs. dinner)")
```
#### Which dining party size group tends to have the highest average total bill amount?
```
sns.barplot(x='size',y='total_bill',data=tips)
plt.title("Highest average total bill amount based party size")
```
#### What is the distribution of tip amounts for each day of the week?
```
sns.boxplot(x='day',y='total_bill',data=tips)
plt.title("Distribution of tip amounts for each day of the week")
```
#### How does the tip amount vary based on the type of service (lunch vs. dinner)?
```
sns.violinplot(x='time',y='tip',data=tips)
plt.title("Tip based on the type of service ")
```
#### Is there any correlation between the total bill amount and the tip amount?
```
sns.scatterplot(data=tips, x='total_bill', y='tip')
correlation_coefficient = tips['total_bill'].corr(tips['tip'])
print("Correlation Coefficient:", correlation_coefficient)
```
#### heatmap
```
tips.corr()
plt.subplots(figsize=(7,5))
sns.heatmap(tips.corr(),annot=True)
```
## OUTPUT
#### Initial dataset
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/0b51c12f-69a4-47e9-8a1b-78d8749d9b03)

#### tips.head()
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/70e71eb8-159a-441b-81b6-d490720f2113)

#### tips.info()
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/ea18b8f4-24c9-40ed-b812-58707ed2f90e)

#### Barplot
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/12b5865c-da1f-496c-a209-a4fc5f09f161)
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/c9f8e81a-c967-4758-9662-2a3661122df2)

#### Boxplot
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/8195dbbb-48a0-4d43-a7b6-c7cbb6403f3e)
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/f9ba2e48-b63d-48a3-b4e5-4b373b46586e)

#### Plot
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/a8ce56ab-0a8f-45d2-b4bf-0e4a97a49762)

#### Violinplot
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/39d6fc57-ad94-42e7-aef7-a959354915b2)

#### Barplot
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/c51c2f31-5b1c-4375-8c09-f50f857fb66f)

#### Boxplot
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/b098d3c4-db06-4043-80cc-4be961716bfc)

#### Violinplot
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/5328b4c0-9577-4c29-aad5-cfb81de959ac)

#### Scatterplot
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/69858954-a359-4a0a-923e-bffdf6767a54)

#### Heatmap
![image](https://github.com/Jenishajustin/ODD2023-Datascience-Ex-09/assets/119405070/8ff6f999-66bb-41e8-b8dd-52b1a6e8b2f3)

## RESULT:
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully based on tips dataset and the data is saved to file.
