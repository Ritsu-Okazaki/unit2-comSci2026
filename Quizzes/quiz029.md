# This is quiz 29

## Code solution
```.py
import requests
from matplotlib import pyplot as plt

server_ip = "192.168.4.137"

callback = requests.get(f"http://{server_ip}/readings")
data = callback.json()
readings = data['readings'][0]

temp_reads = []
pres_reads = []
sum_reads = []

for r in readings:
    if r["sensor_id"] == 11:
        temp_reads.append(r["value"])
    if r["sensor_id"] == 12:
        pres_reads.append(r["value"])

if temp_reads >= pres_reads:
    for i in range(len(temp_reads)):
        sum_reads.append(temp_reads[i]+pres_reads[i])
else:
    for i in range(len(pres_reads)):
        sum_reads.append(temp_reads[i] + pres_reads[i])

plt.subplot(3,1,1)
plt.plot(temp_reads)
plt.subplot(3,1,2)
plt.plot(pres_reads)
plt.subplot(3,1,3)
plt.plot(sum_reads)
plt.show()
```

## Proof of work
![image](https://github.com/user-attachments/assets/8177f528-92ee-4293-8152-f8fc5dffc4a5)
