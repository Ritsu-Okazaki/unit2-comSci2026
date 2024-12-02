# This is quiz 28

## Code solution (main)
```.py
import requests
from matplotlib import pyplot as plt
from my_lib import moving_average
import numpy as np


server_ip = "192.168.4.137"

request = requests.get(f'http://{server_ip}/readings')
data = request.json()

readings = data['readings'][0]

temp = [0]
y = [0]

for r in readings:
    if r['sensor_id'] == 11:
        temp.append(r["value"])
        y.append(y[-1]+1)

temp_segment = temp[600:1600]
temp_smoothed = moving_average(windowSize=3, x=temp_segment)
x = [*range(len(temp_smoothed))]

plt.plot(temp_segment,color="grey")
plt.plot(temp_smoothed)

m,b = np.polyfit(x, temp_smoothed, deg=1)
plt.plot([0,x[-1]],[m*0+b,m*x[-1]+b],color='blue')

a,b,c = np.polyfit(x, temp_smoothed, deg=2)
y_quad = []
for i in x:
    y_quad += [a*i**2 + b*i + c]
plt.plot(y_quad, color='purple')

plt.show()
```

## Code solution (my_lib)
```.py
def moving_average(windowSize:int, x:list)->list:
    x_smoothed = []
    for i in range(0, len(x)-windowSize):
        x_section = x[i:i+windowSize]
        x_average = sum(x_section)/windowSize
        x_smoothed += [x_average]
    return x_smoothed
```

## Proof of work
![image](https://github.com/user-attachments/assets/e431eb34-ac43-4edc-9571-77efa85f767c)
