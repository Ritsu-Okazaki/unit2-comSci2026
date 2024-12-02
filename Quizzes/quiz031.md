# This is quiz 31

## Code solution
```.py
from matplotlib import pyplot as plt

fx_x = []
fx_y = []
ifx_x = []
ifx_y = []
mfx_x = []
mfx_y = []
mifx_x = []
mifx_y = []

step = 4/100

for x in range(100):
    fx_x.append(-2 + x * step)
    fx_y.append(fx_x[-1] ** 2)
    mfx_x.append(-2 + x * step)
    mfx_y.append(-1 * mfx_x[-1] ** 2)

for y in range(100):
    ifx_y.append(-2 + y * step)
    ifx_x.append(ifx_y[-1] ** 2)
    mifx_y.append(-2 + y * step)
    mifx_x.append(-1 * mifx_y[-1] ** 2)


plt.plot(fx_x,fx_y)
plt.plot(ifx_x,ifx_y)
plt.plot(mfx_x,mfx_y)
plt.plot(mifx_x,mifx_y)
plt.show()
```

## Proof of work
![image](https://github.com/user-attachments/assets/b8e38cb8-0a2c-4716-9ffd-68ab79035694)
