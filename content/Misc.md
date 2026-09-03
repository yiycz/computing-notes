---
tags:
  - practical
  - misc
---
> This page is mainly to track the modules/code that I'm not familiar with lol. 

# Dictionary 

### Traverse a dictionary

```python
for key in info:
	print(key, info[key])
```

### Other stuffs

```python
len(d) # return the number of entries
d.clear() # remove all keys
list(d.values()) # all the values of d in list 
list(d.keys()) #all the keys of d in list
```


# datetime

### Current time:

```python
from datetime import datetime

now = datetime.now()
print(now)
```

### Only show hours, minutes and seconds:

```python
print(now.strftime("%H:%M:%S"))
```

### Create an object of a specific time:

```python
datetime(year, month, day, hour, minute, second)
```

### Time difference:

```python
past = datetime(2026, 8, 20, 15, 30, 0)
now = datetime.now()

difference = now - past
print(difference)
print(difference.total_seconds())
```



# csv

### csvreader

```python
reader = csv.reader(file)
```

### csvwriter

```python
file = open("data.csv", "w", newline="")
writer = csv.writer(file)
writer.writerow(["Name", "Age", "Score"])
writer.writerow(["Alice", 17, 85])
writer.writerow(["Bob", 18, 92])
```



# random

```python
import random

number = random.randint(1, 10)
print(number)
```