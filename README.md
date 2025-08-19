# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 19.8.25

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("/content/Sample - Superstore.csv.zip", encoding='ISO-8859-1')


df['Order Date'] = pd.to_datetime(df['Order Date'])
monthly_sales = df.groupby(df['Order Date'].dt.to_period('M'))['Sales'].sum()
monthly_sales.plot(kind='line', figsize=(10, 5), title='Monthly Sales Trend')
plt.ylabel('Sales')
plt.xlabel('Month')
plt.grid(True)
plt.show()
```









# OUTPUT:



<img width="1096" height="607" alt="image" src="https://github.com/user-attachments/assets/32790476-5da9-477a-bb60-7d9b3be3fd19" />



# RESULT:
Thus we have created the python code for plotting the time series of given data.
