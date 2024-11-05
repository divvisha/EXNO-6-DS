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
![Screenshot 2024-11-03 195032](https://github.com/user-attachments/assets/37367215-93c6-40aa-ab20-f4d33796bb5b)
~~~
sns.lineplot(x='total_bill', y='tip', data=df, hue='sex', linestyle='solid', legend='auto')
~~~
![Screenshot 2024-11-03 195102](https://github.com/user-attachments/assets/77186e78-81eb-4917-8f0d-0d7a7512acc3)
~~~
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
~~~
![Screenshot 2024-11-03 195126](https://github.com/user-attachments/assets/497e4da3-af79-44a4-989c-cdf2ea9f1d32)
~~~
plt.figure(figsize=(8, 6))
p1=plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2=plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
~~~
![Screenshot 2024-11-03 195153](https://github.com/user-attachments/assets/60e8d1f7-f3f9-4ea1-a98f-85604b81ab09)
~~~
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
~~~
![Screenshot 2024-11-03 195228](https://github.com/user-attachments/assets/28bd659a-a188-439e-9583-f1c630219495)
~~~
p1=plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2=plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip', width=0.4)
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
~~~
![Screenshot 2024-11-03 195250](https://github.com/user-attachments/assets/8b276d2c-5de5-44db-994e-729edf35bd92)
~~~
dt=sns.load_dataset('tips')
sns.barplot(x='day', y= 'total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
~~~
![Screenshot 2024-11-03 195319](https://github.com/user-attachments/assets/6bb9ecdb-29dc-4c15-8fa8-6f46e27aaefa)
~~~
sns.scatterplot(x='total_bill', y='tip', hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
~~~
![Screenshot 2024-11-03 195358](https://github.com/user-attachments/assets/60637116-4c51-4067-bbc6-90862a454802)
~~~
sns.histplot(data=df, x='total_bill', hue='sex', kde=True)
~~~
![Screenshot 2024-11-03 195424](https://github.com/user-attachments/assets/a94c5f60-ae65-49c2-ae0e-2d5f5690b48c)
~~~
import pandas as pd
sns.boxplot(x=tips['day'], y=tips['total_bill'], hue=tips['sex'],width=0.6, linewidth=1.5,boxprops={"facecolor": "black", "edgecolor": "yellow"},whiskerprops={"color": "red", "linewidth": 1.5},
capprops={"color": "red", "linewidth": 1.5})
~~~
![Screenshot 2024-11-03 195451](https://github.com/user-attachments/assets/461688dc-ce0e-430f-beba-c0670937dcac)
~~~
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6,boxprops={"facecolor": "violet", "edgecolor": "darkblue"},
whiskerprops={"color": "blue", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "blue", "linestyle": "--", "linewidth": 1.5})
~~~
![Screenshot 2024-11-03 195514](https://github.com/user-attachments/assets/809f940c-21d2-4981-9e61-3663171477e4)
~~~
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the week")
plt.ylabel('Total Bill')
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
~~~
![Screenshot 2024-11-03 195544](https://github.com/user-attachments/assets/eb7d3493-f2f0-49d3-a165-b4d59b8456ca)
~~~
sns.set(style = 'whitegrid')
tip= sns.load_dataset('tips')
sns.violinplot(x = 'day', y ='tip', data = tip)
~~~
![Screenshot 2024-11-03 195614](https://github.com/user-attachments/assets/e072f126-1529-4808-9dac-055e14128b12)
~~~
sns.set(style = 'whitegrid')
tip=sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
~~~
![Screenshot 2024-11-03 195638](https://github.com/user-attachments/assets/771734d3-2c7b-40a0-b811-89b04b670e6b)
~~~
sns.set(style="whitegrid")
tips=sns.load_dataset("tips")
sns.violinplot (x="tip", y="day", data=tip)
~~~
![Screenshot 2024-11-03 195700](https://github.com/user-attachments/assets/29af480d-c758-487a-b562-14c65edb09b3)
~~~
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
~~~
![Screenshot 2024-11-03 195726](https://github.com/user-attachments/assets/86588351-a9d8-4cf0-974c-d6805ffcca08)
~~~
sns.kdeplot(data=tips,x='total_bill',hue='time', multiple='layer', linewidth=3,palette='Set2', alpha=0.8)
~~~
![Screenshot 2024-11-03 195749](https://github.com/user-attachments/assets/3a1d8c4e-593a-4cd1-8a5f-60ce344056f4)
~~~
sns.kdeplot(data=tips,x='total_bill',hue='time', multiple='stack', linewidth=3,palette='Set2', alpha=0.8)
~~~
![Screenshot 2024-11-03 195811](https://github.com/user-attachments/assets/1eb39e84-3105-4b4c-9ec6-66dc0bd739cd)
~~~
import numpy as np
data = np.random.randint(low = 1,high = 100, size = (10,10))
print("The data to be plotted:\n")
print(data)
~~~
![Screenshot 2024-11-03 195832](https://github.com/user-attachments/assets/d24e7399-a3ca-4ba1-8e94-457112a250e1)
~~~
hm=sns.heatmap(data=data, annot=True)
~~~
![Screenshot 2024-11-03 195858](https://github.com/user-attachments/assets/cd8c9527-8585-4146-a9be-9bdf7bfef917)
~~~
hm=sns.heatmap(data=data)
~~~
![Screenshot 2024-11-03 195922](https://github.com/user-attachments/assets/d9be6354-88e9-479b-b58a-79c3327fb92d)
~~~
tips=sns.load_dataset("tips")
numeric_cols=tips.select_dtypes (include=np.number).columns 
corr=tips [numeric_cols].corr()
sns.heatmap(corr, annot=True, cmap="plasma", linewidths=0.5)
~~~
![Screenshot 2024-11-05 103121](https://github.com/user-attachments/assets/4ec8ed47-da25-4f05-b6b4-4ed6ab5372e0)

# Result:
  Thus Data Visualization using seaborn python library for the given datas was executed successfully.
