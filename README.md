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
```
import seaborn as sns
import matplotlib.pyplot as plt

df=sns.load_dataset("tips")
df
```
![Screenshot 2024-11-15 082736](https://github.com/user-attachments/assets/c32033c8-a9a6-49fe-9e8f-ea4d225c25e8)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue='sex',linestyle='solid',legend='auto')
```
![Screenshot 2024-11-15 082743](https://github.com/user-attachments/assets/6dde5e05-af90-462f-8759-a3e36ad6b271)

```
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
```
![Screenshot 2024-11-15 082754](https://github.com/user-attachments/assets/2e5325b8-6e4f-4cba-b4b9-c30cd511048b)

```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![Screenshot 2024-11-15 082805](https://github.com/user-attachments/assets/9fe188e7-6b49-48f3-b438-df24aebc69f2)

```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
```
![Screenshot 2024-11-15 082814](https://github.com/user-attachments/assets/550806c0-1cb3-45c2-bf15-4ada63395416)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![Screenshot 2024-11-15 082820](https://github.com/user-attachments/assets/f529ea3c-bcd7-4cac-8c31-c64075a80870)

```
import numpy as np
import pandas as pd
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![Screenshot 2024-11-15 082827](https://github.com/user-attachments/assets/0d16c745-4f26-481c-bdf9-bf83ce095684)

```
sns.boxplot(x='day',y='total_bill',hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"red","edgecolor":"green"},
whiskerprops={"color":"green","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```
![Screenshot 2024-11-15 082833](https://github.com/user-attachments/assets/45496d4c-bccf-4178-bf5c-5554f1af739b)

```
import matplotlib.pyplot as plt
sns.violinplot(x="day", y="total_bill", hue="smoker", data=df, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![Screenshot 2024-11-15 082841](https://github.com/user-attachments/assets/0e689043-2a59-4111-a437-0c6b747f7704)

```
import seaborn as sns
sns.set(style = 'whitegrid',palette='Set2')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```
![Screenshot 2024-11-15 082849](https://github.com/user-attachments/assets/115976bf-1a94-430d-b79f-9a4be23a9a91)

```
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![Screenshot 2024-11-15 082857](https://github.com/user-attachments/assets/724c301c-3e6c-4c59-bb52-e1d94941daea)

```
df=sns.load_dataset("tips")
sns.kdeplot(data=df,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set3',alpha=0.8)
```
![Screenshot 2024-11-15 082903](https://github.com/user-attachments/assets/b36d3599-80e1-4be3-bf44-440871e2f5eb)

```
sns.kdeplot(data=df, x='total_bill', hue='time', multiple='stack', linewidth=3,palette='Set2',alpha=0.8)
```
![Screenshot 2024-11-15 082912](https://github.com/user-attachments/assets/a7faacdf-b6b2-4847-84b3-0cc499db8284)

```
import numpy as np
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(data)
hms=sns.heatmap(data=data)
```
![Screenshot 2024-11-15 082939](https://github.com/user-attachments/assets/3244cddb-0a8c-41db-919a-8a14c61991c6)

```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![Screenshot 2024-11-15 082947](https://github.com/user-attachments/assets/4cecb2be-d7c2-41d9-8abe-bc2fd3d5a1c3)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
