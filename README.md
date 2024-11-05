# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
~~~
import seaborn as sns
import matplotlib.pyplot as plt
df=sns.load_dataset('tips')
df
~~~
![image](https://github.com/user-attachments/assets/d6fb061a-c070-417c-aca3-f376ef6b4d6f)
~~~
sns.lineplot(x='total_bill', y='tip', data=df, hue='sex', linestyle='solid', legend='auto')
~~~
![image](https://github.com/user-attachments/assets/beda70db-fc61-4669-9045-0ad0c6f905eb)
~~~
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
~~~
![image](https://github.com/user-attachments/assets/fb5d217b-1702-49ee-8094-fd09f35450b6)
~~~
plt.figure(figsize=(8, 6))
p1=plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2=plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
~~~
![image](https://github.com/user-attachments/assets/e3b6dee2-0f43-4b61-bc26-4238b1cc55e4)
~~~
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
~~~
![image](https://github.com/user-attachments/assets/e12210f6-1370-4384-b905-107baace8503)
~~~
p1=plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2=plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip', width=0.4)
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
~~~
![image](https://github.com/user-attachments/assets/aebb2aee-fee7-47e9-b795-2e187de501ff)
~~~
dt=sns.load_dataset('tips')
sns.barplot(x='day', y= 'total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
~~~
![image](https://github.com/user-attachments/assets/41f206a9-636e-48de-814e-da183c525160)
~~~
sns.scatterplot(x='total_bill', y='tip', hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
~~~
![image](https://github.com/user-attachments/assets/6d871c39-4ce7-4313-bc6a-00ecf59088a9)
~~~
sns.histplot(data=df, x='total_bill', hue='sex', kde=True)
~~~
![image](https://github.com/user-attachments/assets/8bdcae2b-12a1-48dd-bd31-7c057e820e8e)
~~~
import pandas as pd
sns.boxplot(x=tips['day'], y=tips['total_bill'], hue=tips['sex'],width=0.6, linewidth=1.5,boxprops={"facecolor": "black", "edgecolor": "yellow"},whiskerprops={"color": "red", "linewidth": 1.5},
capprops={"color": "red", "linewidth": 1.5})
~~~
![image](https://github.com/user-attachments/assets/3b8b8c42-6142-4bc9-8b4b-d89c9651c80a)
~~~
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,boxprops={"facecolor": "violet", "edgecolor": "darkblue"},
whiskerprops={"color": "blue", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "blue", "linestyle": "--", "linewidth": 1.5})
~~~
![image](https://github.com/user-attachments/assets/79c43bf3-aeb1-4821-9ba2-686455e0dfdc)
~~~
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel('Total Bill')
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
~~~
![image](https://github.com/user-attachments/assets/e8c223ec-50d0-40a4-a7a2-cae3d276892c)
~~~
sns.set(style = 'whitegrid')
tip= sns.load_dataset('tips')
sns.violinplot(x = 'day', y ='tip', data = tip)
~~~
![image](https://github.com/user-attachments/assets/f983b223-34d1-4053-8af5-2e135c4f9217)
~~~
sns.set(style = 'whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
~~~
![image](https://github.com/user-attachments/assets/26d4279a-fc8a-41d2-820b-e14fbd6fb016)
~~~
sns.set(style="whitegrid")
tips=sns.load_dataset("tips")
sns.violinplot (x="tip", y="day", data=tip)
~~~
![image](https://github.com/user-attachments/assets/fcd1cc09-5450-4789-b336-e32f1d234ce1)
~~~
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
~~~
![image](https://github.com/user-attachments/assets/eaf1c9a4-96f1-4b80-a3f6-aee93eccd45c)
~~~
sns.kdeplot(data=tips,x='total_bill',hue='time', multiple='layer', linewidth=3,palette='Set2', alpha=0.8)
~~~
![image](https://github.com/user-attachments/assets/af9df2a5-d90a-4bf6-a738-87bb96cc39f2)
~~~
sns.kdeplot(data=tips,x='total_bill',hue='time', multiple='stack', linewidth=3,palette='Set2', alpha=0.8)
~~~
![image](https://github.com/user-attachments/assets/6169b055-393e-48ac-9bd6-1c57cdb4bbc2)
~~~
import numpy as np
data = np.random.randint(low = 1,high = 100, size = (10,10))
print("The data to be plotted:\n")
print(data)
~~~
![image](https://github.com/user-attachments/assets/26c140cf-c647-4553-b0ab-1ef12a767228)
~~~
hm=sns.heatmap(data=data, annot=True)
~~~
![image](https://github.com/user-attachments/assets/b9024f82-2d35-480d-ac6c-da206f01f944)
~~~
hm=sns.heatmap(data=data)
~~~
![image](https://github.com/user-attachments/assets/bb9cd9f7-d751-4568-b246-556a166a0bb3)
~~~
tips=sns.load_dataset("tips")
numeric_cols=tips.select_dtypes (include=np.number).columns 
corr=tips [numeric_cols].corr()
sns.heatmap(corr, annot=True, cmap="plasma", linewidths=0.5)
~~~
![image](https://github.com/user-attachments/assets/4cc8afee-7014-4daf-a727-9e438d585162)

# Result:
  Thus Data Visualization using seaborn python library for the given datas was executed successfully.
