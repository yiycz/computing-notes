---
tags:
  - searching
  - practical
---
# Linear Search

### Method

- Read the search key from user
- Compare search key with the start element of the array
- If both matching, return element found and terminate search 
- If both are not matching, move on to the next element and repeat step 3 and 4 until the last element is compared.
- If the search key and last element are still not matching, return element not found and terminate search. 

### Time complexity

Best Case: $O(1)$
Average Case: $O(N)$
Worst Case: $O(N^2)$





# Binary Search

### Iterative

```python
def binary_search_iterative(value, arr, low, high):
	while low <= high: 
		mid = (low+high) // 2
		if arr[mid] == value:
			return mid
		elif arr[mid] > value:
			high = mid - 1
		else:
			low = mid + 1 
	return -1 # DO NOT FORGET THIS
```

### Recursive


```python
def binary_search_recursive(value, arr, low, high):
    if low > high:
        return -1
    else:
        mid = (low+high) // 2
        if arr[mid] == value:
            return mid
        elif arr[mid] > value:
            return binary_search_recursive(value, arr, low, mid-1)
        else:
            return binary_search_recursive(value, arr, mid+1, high)
```


### Time complexity

Best case: $O(1)$
Average Case: $O(logN)$
Worst Case: $O(logN)$




# HashTable Search

### Chaining

```python
class HashTable:
    def __init__(self):
        self.size = 10
        self.array = [[] for _ in range(self.size)]
    
    def hash(self,item):
        return item % self.size

    def insert(self,item):
        self.array[self.hash(item)].append(item)
                       
    def search(self,item):
        return ele in self.array[self.hash(item)]

    def display(self):
        for arr in self.array:
            print(arr)
```

### Linear Probbing 

```python
class HashTable:
    def __init__(self):
        self.size = 10
        self.array = [None for _ in range(self.size)]
    
    def hash(self,item):
        return item % self.size

    def insert(self,item):
        if self.array[self.hash(item)] == None:
            self.array[self.hash(item)] = item
        else:
            curr = self.hash(item)
            count = 1
            while self.array[curr] != None:
                if count == self.size:
                    print("FULL")
                    return
                curr += 1
                count += 1
                if curr >= self.size:
                    curr = 0
            self.array[curr] = item
            
                
                
    def search(self,item):
        if self.array[self.hash(item)] == item:
            return True
        else:
            curr = self.hash(item)
            count = 1
            while self.array[curr] != item:
                if count == self.size:
                    return False
                curr += 1
                count += 1
                if curr >= self.size:
                    curr = 0
            return True

    def display(self):
        print(self.array)
```

### Time complexity 

Worst case: $O(n)$

### Definition

- A hash table stores key-value pairs.
- A hash function converts a key into an array index for fast storage and retrieval.

### Collision Handling

#### Linear Probing
- Check the next available slot until an empty slot is found.
- Uses the entire table.
- Can cause primary clustering.

##### Quadratic Probing

- Probe using increasing squares (1², 2², 3²...).
- Reduces clustering.
- May not visit every slot.
##### Chaining

- Each hash table index stores a linked list.
- Colliding keys are stored in the same linked list.

### Comparisons

##### Linear Probing vs Quadratic Probing

- Linear Probing: 
	- Consecutive slots.
	- More clustering. 
	- Covers the whole table.

- Quadratic Probing
	- Squared jumps.
	- Less clustering.
	- May not cover the whole table.

##### Linear Probing vs Chaining

- Linear Probing
	- Slower insertion.
	- Harder deletion.
	- Usually requires a larger table.
	- Suffers from clustering.

- Chaining
	- Faster insertion.
	- Easier deletion.
	- Smaller table acceptable.
	- Long chains reduce performance.
	
- Worst Case
	- All keys hash to one linked list.
	- Search time becomes O(n).

### Applications

- Database indexing.
- Password hashing/encryption.
- Dictionaries (Maps).
- Caching.

### Characteristics of a Good Hash Function

- The same key always produces the same hash value.
- Uniform distribution of hash values.
- Minimises collisions and clustering.
- Uses all parts of the key.
- Fast to compute.



>[!note]
>-  Clearly, linear search requires $O(n)$ comparisons of the items in the list.
>-  Binary search halves the list in each iteration, so it requires $O(log_2n)$ comparisons. 
>-  But don’t fortget that binary search requires input to be an ordered list. 
>-  For hash table, in ideal circumstances without collision, we found the item in one step, i.e. $O(1)$. 
>-  When collision occurs, it requires $O(n)$. Hence a good hash function is very important.
>-  On the other hand, hash table may require more spaces as well. Each searching algorithm has its own pros and cons.
