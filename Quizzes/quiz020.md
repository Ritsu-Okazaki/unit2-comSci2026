# This is quiz 20

## Code solution
```.py
from matplotlib import pyplot as plt
import random
random.seed(1234)
plt.style.use('ggplot')

def produce(n=5, m=3, s=2):
    x, y = [], []
    for _ in range(n):
        x.append(random.randint(0,100))
        y.append(x[-1]**(0.5*(m/s)**2))
    return x,y

x, y = produce(n=100)
plt.plot(x, y)
plt.show()
```

## Flow diagram
![image](https://github.com/user-attachments/assets/6323a4b1-3e8c-4eaf-bf87-df981bacdb18)

## Proof of work
![image](https://github.com/user-attachments/assets/f1f0b233-c122-4a24-8208-20006c5cd029)
