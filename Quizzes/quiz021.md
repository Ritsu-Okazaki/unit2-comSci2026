# This is quiz 21

## Code solution
```.py
from matplotlib import pyplot as plt

x, y = [], []

plt.style.use("ggplot")

start = -10
step = 0.01
for i in range(int(20/step)):
    x.append(start+ i*step)
    y.append(2*((x[-1]+5)**2))
plt.plot(x,y,linewidth=2,color="red")
line_x = [-5,-5]
line_y = [0, 450]
plt.plot(line_x, line_y, linewidth=3,color="cyan", linestyle="dashed")
plt.xlabel("x variable")
plt.ylabel("y variable")
plt.title("parabola $2(x+5)^2$")
plt.show()
```

## Flow diagram
![image](https://github.com/user-attachments/assets/03445f7b-efda-41fc-9a85-bb5a0b0945f5)

## Proof of work
![image](https://github.com/user-attachments/assets/b6ab9e51-f952-4cb8-bcbc-22588a66c92f)
