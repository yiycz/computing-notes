---
tags:
  - practical
  - data-representation
---
# Binary to Denary

```python 
def B2D(binary):
    n = 0
    for i in range(len(binary)):
        n += int(binary[i]) * (2 ** (len(binary) - 1 - i)) 
    return n
```

Tips:

```python
n += int(binary[i]) * (2 ** (len(binary) - 1 - i)) 
# 5,4,3,2,1,0 not 0,1,2,3,4,5
```


# Denary to Binary

```python 
def D2B(number):
    s = ""
    while number!=0:
        s = str(number%2) + s 
        number //= 2
    return s  
```

Tips:

```python
s = str(number%2) + s # reverse order
```

# Denary to Hexi

```python
def D2H(number):
    hexdict = "0123456789ABCDEF"
    s = ""
    while number != 0:
        s = hexdict[number % 16] + s 
        number //= 16
    return s
```

Tips:

```python
s = hexdict[number % 16] + s 
```


# Hexi to Denary 

```python
def H2D(hexi):
    hexlist = "0123456789ABCDEF"
    n = 0
    for i in range(len(hexi)):
        value = hexlist.index(hexi[i]) 
        n += value * (16 ** (len(hexi) - i - 1))
    return n
```

Tips:

```python
value = hexlist.index(hexi[i]) # To find the index 
```
