# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 20.4.2026

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
6. Display the graph.

   
# PROGRAM:


```python

from matplotlib import pyplot as plt
import pandas as pd
df=pd.read_csv("/content/weather_2013_to_2024.csv")
df.head()
df['DATE'] = pd.to_datetime(df['DATE'])
df.set_index('DATE', inplace=True)
print(df.dtypes)
df['heat_index'].plot(kind='line', label='heat_index',color="blue")
plt.title('Time Series Plot of Temperature')
plt.xlabel('Date')
plt.ylabel('Temperature')
plt.legend()
plt.grid(True)
plt.show()

```

# OUTPUT:


<img width="1772" height="271" alt="image" src="https://github.com/user-attachments/assets/d16270cb-0daf-48ee-9335-b12a00430a31" />

<img width="424" height="585" alt="image" src="https://github.com/user-attachments/assets/83a9c6b0-c788-4b20-a90e-a9f032414da7" />

<img width="784" height="496" alt="image" src="https://github.com/user-attachments/assets/fc8632e9-9a50-439c-acd8-f40adc3292fc" />



# RESULT:
Thus we have created the python code for plotting the time series of given data.
