# This is quiz 26

## Code solution (SL)
```.py
def flip(in_dict):
    out_dict = {}
    for a,b in in_dict.items():
        out_dict[b] = a
    return out_dict

print(flip({'a':1,'b':2,'c':3}))
```

## Paper solution
![20241202_231543](https://github.com/user-attachments/assets/c2e9bb6b-44ae-4b4c-9537-3484ca36427b)

## Proof of work (SL)
![image](https://github.com/user-attachments/assets/3229c45b-ac47-4834-bbbf-55ef83f3a2ac)

## Code solution (HL)
```.py
def flip(in_dict):
    out_dict = {}
    for a,b in in_dict.items():
        if b in out_dict:
            out_dict[b].append(a)
        else:
            out_dict[b] = [a]
    return out_dict

print(flip({'q1':True,'q2':False,'q3':True}))
```

## Proof of work (HL)
![image](https://github.com/user-attachments/assets/b1bcf430-5f9e-4455-aeac-f908081ed538)
