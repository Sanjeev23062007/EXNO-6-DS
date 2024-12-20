# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
## Name: SANJEEV 
## Reg no:24900568
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
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```

![image](https://github.com/user-attachments/assets/4637091a-300a-4b05-b2b3-d40116f6cb45)

```
df = sns.load_dataset("tips")
df
```

![image](https://github.com/user-attachments/assets/7ac5aaf9-3407-4e1f-95ab-06b5e877dec1)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```

![image](https://github.com/user-attachments/assets/b2afcc0e-49c9-4933-827c-27f87ca9961b)

```
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

![image](https://github.com/user-attachments/assets/ea9b3276-1367-4885-9f1a-87bc26285260)

```
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

![image](https://github.com/user-attachments/assets/3d7c2768-176d-4fd4-9801-78cd469cadfe)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```

![image](https://github.com/user-attachments/assets/6c851984-1d73-4ee7-a2da-d70184281de7)

```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```

![image](https://github.com/user-attachments/assets/9f33b52f-668b-420b-9d16-e8beed6b2ad3)

```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```

![image](https://github.com/user-attachments/assets/0d62f0d9-b615-4517-a3a5-19cbb80fc5ea)

```
tit=pd.read_csv("titanic_dataset.csv")
tit
```

![image](https://github.com/user-attachments/assets/a93fd8d7-af3b-4d5a-ac8f-6cb7f1872cb0)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```

![image](https://github.com/user-attachments/assets/c408b72c-640a-45e2-a90d-695a4dc0b8f1)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```

![image](https://github.com/user-attachments/assets/56c23bec-234a-453e-9865-6ad1e6e02dd8)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![image](https://github.com/user-attachments/assets/c2ccf89a-4c63-400a-b81b-92b2950dc54d)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```

![image](https://github.com/user-attachments/assets/5a6eb151-2711-4dd6-80ca-f3e0dbde56ce)

```
sns.histplot(data = num_var, kde = True)
```

![image](https://github.com/user-attachments/assets/8385766a-4811-4492-ac0e-419723d59a21)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

![image](https://github.com/user-attachments/assets/bd4fd0d7-f350-40c2-916f-3b96d60f13f4)

```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

![image](https://github.com/user-attachments/assets/41cb4555-96af-4444-bbde-3e7998ae72a1)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```

![image](https://github.com/user-attachments/assets/23fa353a-5508-4d3b-898a-224bcba27454)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```

![image](https://github.com/user-attachments/assets/8ca3d295-5b74-498f-916d-e67b8418e620)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

![image](https://github.com/user-attachments/assets/5fd55764-1aa8-4839-be28-ce0fa984ed42)

```
mart=pd.read_csv("titanic_dataset.csv")
mart
```

![image](https://github.com/user-attachments/assets/8c030d68-38e1-4b82-8a7d-4f8ffb920409)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```

![image](https://github.com/user-attachments/assets/8491d5b4-ecc4-456c-8e6d-fdce3bc750d0)

```
sns.kdeplot(data=mart,x='PassengerId')
```

![image](https://github.com/user-attachments/assets/111b83af-1487-45af-9eed-9f6af39db760)

```
import seaborn as sns
import pandas as pd
```

# Assuming 'mart' is your DataFrame

```
mart=pd.read_csv("titanic_dataset.csv")
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]

sns.kdeplot(data=mart, x='Age')
```

![image](https://github.com/user-attachments/assets/b4e22b7e-b4fc-4135-b77e-2482a8fa8939)

```
sns.kdeplot(data=mart)
```

![image](https://github.com/user-attachments/assets/b5c76ac5-5249-4c71-9672-8be0aecac514)

```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```

![image](https://github.com/user-attachments/assets/984a6fa3-80b6-4378-9eb0-c72770c13bd0)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

![image](https://github.com/user-attachments/assets/d3471dbc-1029-4124-9155-f3c637442f7f)

```
import numpy as np  # Import numpy and assign it the alias 'np'
import seaborn as sns

data = np.random.randint(low=1, high=100, size=(10, 10))  # Now np is defined and can be used
hm = sns.heatmap(data=data, annot=True)
```

![image](https://github.com/user-attachments/assets/ea6fc737-21e9-4f8c-bd4d-d837402f13f0)

```
hm=sns.heatmap(data=data)
```

![image](https://github.com/user-attachments/assets/1b138467-f118-48f2-b8c8-b5dd487da6dd)

# Result:
 Thus, all the data visualization techniques of seaborn has been implemented
