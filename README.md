![Screenshot 2025-03-28 024740](https://github.com/user-attachments/assets/4e411958-6a4b-45a3-a5c5-dee429bd7344)
The project is done in jupyter notebook
codes:
import pandas as pd
df = pd.read_csv(r"C:\Users\shaur\Downloads\titanic.csv")
df.head()
print(df.info())
print(df.describe())
print(df.isnull().sum())  # Check for missing values
df = df[['Survived', 'Pclass', 'Sex', 'Age', 'Fare']]
children = df[df["Age"] < 18]
print(children)
df.loc[:, 'Age'] = df['Age'].fillna(df['Age'].median())
df.fillna({'Age': df['Age'].median()}, inplace=True)
print(df)
