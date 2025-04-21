# numpy-pandas
import numpy as np
a=np.array([1,2,3,4,5,6,7,8,9,10])
b=a.reshape(2,5)
print(b)


c=np.array([1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20])
print(c[6:15])

import pandas as pd
data= pd.Series(['apples', 'bananas', 'oranges'])
index_1=(['3','2','1'])
data.index=index_1
data1=pd.Series(['pears'])
index_2=(['4'])
data1.index=index_2
data3=data._append(data1)
print(data3)

import pandas as pd

data = {'name': ['Alice', 'Bob', 'Charlie', 'David', 'Eve', 'Frank', 'Grace', 'Henry', 'Ivy', 'Jack'],
        'age': [25, 30, 28, 32, 27, 29, 31, 26, 33, 34],
        'gender': ['Female', 'Male', 'Male', 'Male', 'Female', 'Male', 'Female', 'Male', 'Female', 'Male']}

data1 = pd.DataFrame(data)

print(data1)

data1["occupation"] = ["Programmer", "Manager", "Analyst", "Programmer", "Manager", "Analyst", "Programmer", "Manager", "Analyst", "Programmer"]

print(data1)

data1_age=data1[data1['age']>30]
print(data1_age)

data1.to_csv('data1.csv')
data1_read=pd.read_csv('data1.csv')
print(data1_read)
