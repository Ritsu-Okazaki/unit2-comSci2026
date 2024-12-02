# This is quiz 30

## Code solution
```.py
from matplotlib import pyplot as plt
import requests
from matplotlib.gridspec import GridSpec

server_ip = "192.168.4.137"

callback = requests.get(f"http://{server_ip}/readings")
data = callback.json()
readings = data['readings'][0]

s10reads = []
s11reads = []
s1011sums = []

for r in readings:
    if r["sensor_id"] == 10:
        s10reads.append(r["value"])
    if r["sensor_id"] == 11:
        s11reads.append(r["value"])

for i,j in zip(s10reads,s11reads):
    s1011sums.append(i+j)

fig = plt.figure(figsize=(10,10))
grid = GridSpec(nrows=3, ncols=4, figure=fig)
box1 = fig.add_subplot(grid[0:3, 1:3])
plt.plot(s1011sums)

box2 = fig.add_subplot(grid[1,0])
plt.plot(s10reads)

box3 = fig.add_subplot(grid[1,3])
plt.plot(s11reads)

plt.show()
```

## Proof of work
![image](https://github.com/user-attachments/assets/96396b9f-5f05-4445-954f-154904a2990c)
