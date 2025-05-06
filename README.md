# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
## STEP 1:Include the necessary Library.

## STEP 2:Read the given Data.

## STEP 3:Apply data visualization techniques to identify the patterns of the data.

## STEP 4:Apply the various data visualization tools wherever necessary.

## STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```python
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![download](https://github.com/user-attachments/assets/bf2c4b2c-c92c-48d5-8cdf-6e565e0ee77c)
```python
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/6aaae472-ec06-4bbc-a0d2-0f73fa4b7563)
```python
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![download](https://github.com/user-attachments/assets/c8df62c3-4232-4c23-b108-9fa15d4eae25)
```python
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![download](https://github.com/user-attachments/assets/9fdda7c8-1007-4fdd-8cf5-57e95af529d7)

```python
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![download](https://github.com/user-attachments/assets/abe846d4-9f8b-4eb1-a995-3432607d8ace)
```python
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![download](https://github.com/user-attachments/assets/e2429c54-dabd-424c-880c-f1a5f4a8b06d)
```python
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![download](https://github.com/user-attachments/assets/c38a0245-6e9d-4daf-8231-3d212542048e)
```python
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![download](https://github.com/user-attachments/assets/fa18a4bb-b95d-49e6-a8e1-440157036271)
```python
from google.colab import drive
drive.mount('/content/drive')
```
![image](https://github.com/user-attachments/assets/5f903b32-35ea-4004-bc52-cfaa13a489bb)
```python
ls drive/MyDrive/DS2024/titanic_dataset.csv
```
![image](https://github.com/user-attachments/assets/2a4cbdbe-81d7-4095-924a-7525f0d36c16)

```python
tit=pd.read_csv("/content/drive/MyDrive/titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/b61b01b6-7d01-49e2-bcac-4f68ac73f62a)
```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```
![download](https://github.com/user-attachments/assets/6c6c0f9c-4778-41ad-bfb3-25edd4551ec7)
```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![download](https://github.com/user-attachments/assets/1d38470d-29c8-4310-b6bf-8d82fecf076d)
```python
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![download](https://github.com/user-attachments/assets/7351251f-995c-4a13-b873-dba4288f1550)
```python
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/8439aceb-5959-41d2-9da8-d4f84fdb9879)
```python
sns.histplot(data = num_var, kde = True)
```
![download](https://github.com/user-attachments/assets/a45f9296-ee58-4a78-98be-e22787d7ba32)
```python
df=pd.read_csv("/content/drive/MyDrive/titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![download](https://github.com/user-attachments/assets/e8259875-9398-4a10-9d35-d046ff81cc63)
```python
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![download](https://github.com/user-attachments/assets/21ce9a51-12ad-4920-bcd8-57018f725ff5)
```python
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![download](https://github.com/user-attachments/assets/f82b994b-6115-42b4-b181-1c8587ba1227)
```python
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin P``lot of Total Bill by Day and Smoker Status")
```
![download](https://github.com/user-attachments/assets/63d9ab36-871a-4437-843f-7d1c1dbc8fae)
```python
mart=pd.read_csv("/content/drive/MyDrive/titanic_dataset.csv")
mart
```
![image](https://github.com/user-attachments/assets/5639837d-42ca-4ea2-ad2e-ac0ad2df745a)
```python
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![image](https://github.com/user-attachments/assets/c2a18efe-3324-478f-945b-c257a78df778)
```python
sns.kdeplot(data=mart,x='PassengerId')
``
![download](https://github.com/user-attachments/assets/f99156b5-75fc-4c48-9349-be47a950443b)
```python
sns.kdeplot(data=mart,x='Age')
```
![download](https://github.com/user-attachments/assets/5acc0ed0-b8f6-4bd1-b21c-9d9336750a91)
```python
sns.kdeplot(data=mart)
```
![download](https://github.com/user-attachments/assets/a0720b47-178f-4ce4-91db-7b48c7aa36ba)
```python
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![download](https://github.com/user-attachments/assets/a4d1d436-5ad5-4f5c-a704-5b4fefdd119d)
```python
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![download](https://github.com/user-attachments/assets/b80661c5-b542-491c-b038-1ce54e550e44)
```python
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```
![download](https://github.com/user-attachments/assets/dc51c4bb-7ce4-4eb2-9fbb-409024624305)
```python
hm=sns.heatmap(data=data)
```
![download](https://github.com/user-attachments/assets/7b878fea-1e13-48b6-a2af-8f75b0b9fec2)
# Result:
 Include your result here
