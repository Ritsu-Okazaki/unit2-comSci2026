# This is quiz 17

## Code solution
```.py
def get_truth():
    header = "| A | B | C |"
    print(header)
    a, b, c = False, False, False
    for i in range(1, 9):
        line  = f"| {int(a)} | {int(b)} | {int(c)} |"
        if i % 4 == 0:
            a = not a
        if i % 2 == 0:
            b = not b
        c = not c
        print(line)

get_truth()
```

## Flow diagram
![image](https://github.com/user-attachments/assets/3f5cc394-f8f1-45f4-9fc6-a8be8d3fa9a8)

## Proof of work
![image](https://github.com/user-attachments/assets/3984f406-9515-448e-8513-8432019c4178)
