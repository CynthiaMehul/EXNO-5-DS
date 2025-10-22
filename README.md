# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Program:
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline

x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]

plt.plot(x, y, label="Line 1")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Simple Line Graph")
plt.legend()
plt.show()

x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]

plt.plot(x1, y1, label="Line 1", marker='o')
plt.plot(x2, y2, label="Line 2", marker='s')
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Two Lines in One Graph")
plt.legend()
plt.show()

x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]

plt.plot(x_values, y_values, label="y = x^2")
plt.fill_between(x_values, y_values, color='lightblue', alpha=0.5)
plt.title("Line Graph with Fill Between")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.show()

x = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
y = np.array([2, 4, 5, 7, 8, 8, 9, 10, 11, 12])

X_smooth = np.linspace(x.min(), x.max(), 300)
spline = make_interp_spline(x, y)
Y_smooth = spline(X_smooth)

plt.plot(X_smooth, Y_smooth, label="Cubic Spline Interpolation")
plt.title("Interpolated Curve")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.show()

values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]

plt.bar(names, values, color='skyblue')
plt.title("Bar Chart")
plt.xlabel("Categories")
plt.ylabel("Values")
plt.show()

df = sns.load_dataset("tips")

avg_total_bill = df.groupby("day")['total_bill'].mean()
avg_tip = df.groupby("day")['tip'].mean()

p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()

x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]

plt.scatter(x_values, y_values)
plt.title("Basic Scatter Plot")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.show()

x = [1,2,3,4,5,6,7,8,9,10]
y = [2,4,5,7,6,8,9,11,12,12]

plt.scatter(x, y, label="stars", color="green", marker="*", s=30)
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.title("Scatter Plot Example")
plt.legend()
plt.show()

activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']

plt.pie(slices, labels=activities, colors=colors, autopct='%1.1f%%')
plt.title("Daily Activities Pie Chart")
plt.show()

# Output:
Line Graph

<img width="739" height="566" alt="image" src="https://github.com/user-attachments/assets/db9be05c-cbca-4c69-9c60-d6d13c3f9033" />

Multi Line Graph

<img width="724" height="556" alt="image" src="https://github.com/user-attachments/assets/1a1ebe30-9435-43b1-807b-66c9450439b1" />

Area Graph

<img width="753" height="561" alt="image" src="https://github.com/user-attachments/assets/9126c409-7484-4e2f-a161-c427b1178684" />

Spline Graph

<img width="736" height="561" alt="image" src="https://github.com/user-attachments/assets/fafd83a5-9510-4878-baff-18fcbc5978e2" />

Bar Chart

<img width="732" height="555" alt="image" src="https://github.com/user-attachments/assets/43299ec2-5b57-49b7-a743-a79f230a7da6" />


Stacked Bar Chart

<img width="733" height="569" alt="image" src="https://github.com/user-attachments/assets/8473e180-0247-4ec7-ac5a-03051a9e40b8" />


Scatter Plot

<img width="753" height="559" alt="image" src="https://github.com/user-attachments/assets/0e6d748c-05dc-4e32-b94b-0d02491be10e" />

<img width="748" height="564" alt="image" src="https://github.com/user-attachments/assets/ec4cee93-5790-4dbe-bf6e-bf87838e5929" />

Pie Chart

<img width="552" height="462" alt="image" src="https://github.com/user-attachments/assets/2fd456a4-8da0-4d7e-b598-0410e95a1697" />

# Result:
Therefore, various graphs are plotted to perform data visualization using matplot library in python successfully.

Line Graphs: These are commonly used for data that involves time (time series datasets). It is used for continous data.

MultiLine Graphs: These are also used for continous data when there are two or more features to compare.

Area Graph: This is similar to line graph but the area between the axes and the line drawn is filled with color. This makes the graph more visually appealing. 

Spline Graph: This is similar to line graph but the lines between the data points are smoothly connected. This enables us to extract output at every input point.

Bar Graph: This is important when comparing a numerical value with a categorical value. It shows simple idea about them.

Stacked Bar Graph: This is used when two or more features must be compared.

Scatter Plot: This simply plots points between two or more features.

Pie Chart: This shows the proportion of each feature involved in a circular graph. It can be used when the difference between each feature is high.
