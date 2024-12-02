# This is quiz 32

## Code solution
```.py
def mystery(a:list, b:list)->list:
    empty_list = []
    for i in a:
        for j in b:
            if i == j:
                empty_list.append(i)
    return empty_list

print(mystery(["a","b","c","d","e","f"],["e","f","g","h","i","j"]))
```

## Proof of work
![image](https://github.com/user-attachments/assets/bf2a2d7c-4c66-4582-98d7-44cf4c4b2ef1)
