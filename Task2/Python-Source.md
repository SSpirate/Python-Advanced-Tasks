# :star2: Python-Source:
          
## Solution:
```sh
import string


def xor(x):
    return ''.join(chr(ord(i)^10) for i in x)


def shift(x):
    upper = string.ascii_uppercase
    lower = string.ascii_lowercase
    digits = string.digits
    n = []
    for i in x:
        if i.isupper() is True:
            n.append(upper[(upper.index(i)+3)%26])
        elif i.islower() is True:
            n.append(lower[(lower.index(i)+3)%26])
        elif i.isdigit() is True:
            n.append(digits[(digits.index(i)+3)%10])
    return n

def encode(x):
    p = (xor(shift(arr))).encode('utf-8')   
    return (p. hex())
if __name__=="__main__":
    print ("Decode the following string to find the flag:")
    print ("667b6c7d63673c733c323c3c7b333e7b3c3c3e7b333e3232393c3d32")
    print ("Enter what you got after decoding:")

    arr = "inctfj3v3533n61n331n61550345"
    

    your_code = encode(arr)
    print(your_code)

    if your_code == ("667b6c7d63673c733c323c3c7b333e7b3c3c3e7b333e3232393c3d32"):
        print ("Yeah!....You are a Genius")
    else:
        print ("Oops....Try again")
        print ("Looking at the source code might help")

```
## Decoded Text:
    * inctfj3v3533n61n331n61550345
## Output:
    * Yeah!....You are a Genius
    
