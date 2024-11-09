# This is quiz 18

## Code solution
```.py
def get_truth():
    header = "| A | B | C |AB + not B + not CB|"
    print(header)
    a, b, c, r = False, False, False, False
    for i in range(1, 9):
        line  = f"| {int(a)} | {int(b)} | {int(c)} |         {int(r)}         |"
        if i % 4 == 0:
            a = not a
        if i % 2 == 0:
            b = not b
        c = not c

        if bool(a*b) + (not b) + (not bool(c*b)) == True:
            r = True
        else:
            r = False
            
        print(line)

get_truth()
```

## Flow diagram

## Proof of work
![image](https://github.com/user-attachments/assets/93508463-a8f1-43d8-8aa8-4ed2858c8ea1)
