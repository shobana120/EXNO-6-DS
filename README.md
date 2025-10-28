# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
# NAME : SHOBANA B
# REG NO :212224230262
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
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("titanic_dataset.csv")
 df.head()
```

<img width="825" height="194" alt="image" src="https://github.com/user-attachments/assets/b1ef8389-3978-4372-ad64-8d50f26ec332" />


# Line Plot:
```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```

<img width="433" height="352" alt="image" src="https://github.com/user-attachments/assets/29bedc48-e5d6-4a99-8022-f282e4965447" />


# Multi Line Plot:
```
 x=[1,2,3,4,5]
 y1=[3,5,2,6,1]
 y2=[1,6,4,3,8]
 y3=[5,2,7,1,4]
 sns.lineplot(x=x,y=y1)
 sns.lineplot(x=x,y=y2)
 sns.lineplot(x=x,y=y3)
 plt.title('Multi Line Plot')
```

<img width="442" height="352" alt="image" src="https://github.com/user-attachments/assets/f7a7c36f-4468-479f-b762-21fcb4ae26c3" />


## TO VISUALIZE RELATIONSHIPS
# Bar Chart:
```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```

<img width="574" height="397" alt="image" src="https://github.com/user-attachments/assets/ddfe210f-3d3f-491c-bae9-2b66ce83abc7" />


# Scatter Plot:
```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```

<img width="516" height="354" alt="image" src="https://github.com/user-attachments/assets/580e193f-d976-49a1-a0cc-ad7e4c004734" />


# Bubble Chart;
```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```

<img width="523" height="355" alt="image" src="https://github.com/user-attachments/assets/56754738-fe33-4b14-a1b8-51e3951d5780" />


##  TO CAPTURE DISTRIBUTIONS
# Histogram:
```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="505" height="347" alt="image" src="https://github.com/user-attachments/assets/9d621865-3aa8-41b1-9392-80753f8c296a" />


# Box Plot:
```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```

<img width="525" height="384" alt="image" src="https://github.com/user-attachments/assets/b61e838b-4970-482b-b055-e9cfb06e0e5e" />


# Violin Plot:
```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```

<img width="522" height="358" alt="image" src="https://github.com/user-attachments/assets/cb50ea47-d9c8-4797-94f3-bbcf7c123b09" />


# Density Plot:
```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```

<img width="525" height="368" alt="image" src="https://github.com/user-attachments/assets/3d997c2a-7d48-4e76-8243-763ecdab1f8c" />


# Heat Map:
```
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```

<img width="515" height="390" alt="image" src="https://github.com/user-attachments/assets/7e571e7c-401d-42dc-9beb-d07f4567b0f7" />



# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
