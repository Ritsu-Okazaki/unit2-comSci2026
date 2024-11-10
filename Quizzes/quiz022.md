# This is quiz 22

## Code solution
```py
from matplotlib import pyplot as plt

plt.style.use('ggplot')

x, y = [], []

steps = 100
# y = x, y = -x

start = -10
step = 0.01
for i in range(int(20/step)):
    x.append(start+ i*step)
    y.append(abs(x[-1]))

plt.xlabel("x")
plt.ylabel("$f(x)=|x|$")
plt.plot(x, y)
plt.show()
```

## Flow diagram
![image](https://github.com/user-attachments/assets/5f33a50e-6ac8-4450-b30b-11098bbcd0ba)

## Proof of work
![image](https://github.com/user-attachments/assets/40f2dfba-7f2d-4399-b7de-67f5d1828242)
