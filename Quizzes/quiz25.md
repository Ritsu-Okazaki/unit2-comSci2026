# This is quiz 25

## Code solution
```.py
def count_letter(my_dict:list, msg:str):
    for i in range(len(msg)):
        if my_dict.get(msg[i]) != None:
            my_dict[msg[i]] += 1
    return my_dict

print(count_letter({'a':0,'e':0,'i':0,'o':0,'u':0}, "Why did I choose CS?"))
```

## Paper solution
![quiz25](https://github.com/user-attachments/assets/8fa1e0d0-3ba9-4891-9093-fd18bd2d7f67)

## Proof of work
![image](https://github.com/user-attachments/assets/828cce2c-c317-4c6a-862b-4477c88eea0f)
