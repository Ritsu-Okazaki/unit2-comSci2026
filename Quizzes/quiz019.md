# This is quiz 19

## Code solution
```.py
import random
random.seed(1234)

def produce(n=5, m=3, s=2):
    for _ in range(n):
        x = random.randint(0,100)
        y = x**(((m/s)**2)/2)
        xmargin = " "*(3-len(str(x)))
        ymargin = " "*(7-len(f"{y:.2f}"))
        row = f"| {x}{xmargin}| {y:.2f}{ymargin}|"
        print(row)

produce()
```

## Flow diagram


## Proof of work
![image](https://github.com/user-attachments/assets/797e8a26-cce4-476b-87f8-7853eba0408b)
