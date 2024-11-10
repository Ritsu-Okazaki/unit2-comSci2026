# This is quiz 23

## Code solution
```.py
from matplotlib import pyplot as plt
import numpy as np

data = [57.0, 56.0, 57.0, 56.0, 55.0, 55.0, 54.0, 54.0, 53.0, 53.0, 54.0, 53.0, 53.0, 52.0, 52.0, 51.0, 51.0, 51.0, 50.0, 50.0, 49.0, 50.0, 49.0, 49.0, 48.0, 49.0, 49.0, 48.0, 48.0, 48.0, 49.0]
mins = []
model = []

for i in range(len(data)):
    mins.append(i*10)
plt.plot(mins, data)
m, b = np.polyfit(mins, data, 1)
for i in range(len(mins)):
    model.append(m*mins[i]+b)
plt.plot(mins, model)

plt.show()
```

## Flow diagram
![image](https://github.com/user-attachments/assets/eb247ebc-a30e-4b39-a2a0-786e7a89f725)

## Proof of work
![image](https://github.com/user-attachments/assets/3e327017-98dc-4ca6-9388-9c458d92fa85)
