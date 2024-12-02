# This is quiz 27

## Code solution (a)
```.py
def sort_dict(in_dict):
    out_dict = {}
    while len(in_dict) != 0:
        for k,v in list(in_dict.items()):
            if type(v) is str:
                out_dict[k] = v
                del in_dict[k]
        for k,v in list(in_dict.items()):
            if type(v) is int:
                if v == min(in_dict.values()):
                    out_dict[k] = v
                    del in_dict[k]
    return out_dict

print(sort_dict({'apple': 'red', 'banana': 2, 'orange': 'orange', 'grape': 1, 'kiwi': 'brown', 'pear': 8}))
```

## Paper solution
![20241203_004151](https://github.com/user-attachments/assets/6a59beb1-2e30-40aa-9691-2bba12c793fa)

## Proof of work (a)
![image](https://github.com/user-attachments/assets/1c4d7dbb-d2a1-4032-a4c2-35f915ba6078)

## Code solution (b)
```.py
import matplotlib
from matplotlib import pyplot as plt
import math

step = 100
x=[]
y=[]
for i in range(100):
    x.append(i/100)
    y.append(math.sin(2*x[-1]*math.pi))

plt.plot(x,y)
plt.show()
```

## Proof of work (b)
![image](https://github.com/user-attachments/assets/231c532e-3b4d-4c34-a71a-2b04538baec5)
