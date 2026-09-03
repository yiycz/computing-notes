---
tags:
  - sorting
  - practical
---
# Bubble Sort

### Iterative

```python
def bubble_sort_interative(arr):
    for i in range(1,len(arr)): 
        for j in range(0,len(arr) - i): 
            if arr[j] > arr[j+1]:
                arr[j] , arr[j+1] = arr[j+1], arr[j]
```

### Recursive

```python
def bubble_sort_recursive(arr, upperbound):
    if upperbound == 1:
        return 
    swapped = False
    for j in range(0,upperbound-1):
        if arr[j] > arr[j+1]:
             arr[j] , arr[j+1] = arr[j+1], arr[j]
             swapped = True
    if swapped == False:
        return 
    recursiveBubbleSort(arr, upperBound - 1)
```


### Method

- In each pass of the bubble sort:
	- The item in the first position is compared with the item in the second position. If they are out of order, they are exchanged; if they are in order, they are left alone.
	- The item now in the second position is compared with the item in the third position. If they are out of order, they are exchanged; if they are in order, they are left alone.
	- The item now in the third position is compared with the item in the forth position ..
	- The steps in the pass continue until each item has been checked. 

### Time Complexity 

Worst-Case: $O(N^2)$
Avg-Case: $O(N^2)$
Best Case: $O(N)$












# Insertion

### Iterative

```python
def insertion_sort_iterative(arr):
    for i in range(0, len(arr)):
        item_to_insert = arr[i] # every first item and check forward
        prev = i - 1
        while prev >= 0 and item_to_insert < arr[prev]: #swap
            arr[prev+1] = arr[prev] # move one forward cos larger
            prev = prev - 1 # move prev index forward to the next element
        arr[prev+1] = item_to_insert # empty sort for insertion
```

### Recursive

```python
def insertion_sort_recursive(arr, n): # n is length
    if n > 1:
        insertion_sort_recursive(arr, n-1) 
        item_to_insert = arr[n-1]
        prev = n - 2
        while prev >= 0 and item_to_insert < arr[prev]: #swap
            arr[prev+1] = arr[prev] # move one forward cos larger
            prev = prev - 1 # move prev index forward to the next element
        arr[prev+1] = item_to_insert # empty sort for insertion
    else:
        return
```


### Method

- Take left as sorted, right as unsorted
- If right is only 1 value; sorted
- Else:
	- Compare value before and current value (start index from 1):
	- If current<before, switch place of current with before
	- Keep going until
	- Current place is 0 (smallest value so sent to front): or current $>$ before, in which case continue

### Time complexity 

Best for small size arrays
Time complexity of $O(n^2)$




# Quick Sort

### In-place

```python
def quicksort_ip(arr, first, last): # first, last
    # low, high are those which change
    low = first
    high = last
    pivot = arr[(first+last) // 2]

    while(low <= high):
        while arr[low] < pivot:
            low += 1
        while arr[high] > pivot:
            high -= 1
        if low <= high:
            arr[low], arr[high] = arr[high], arr[low]
            low += 1
            high -= 1

    if first < high:
        quicksort_ip(arr,first,high)
    
    if low < last:
        quicksort_ip(arr,low,last)
```


### Not In-place

```python
def quicksort_nip(arr):
    if len(arr) <= 1:
        return arr # MISSING DURING PRACTICE
    else:
        pivot = arr[0]
        less = []
        more = []

        for i in range(1,len(arr)): 
            if arr[i] > pivot:
                more.append(arr[i])
            else:
                less.append(arr[i])
        
        less = quicksort_nip(less)
        more = quicksort_nip(more)
	    return less + [pivot] + more
```

### Method

 - If the array `arr` has no elements or only one element, then it is sorted. Otherwise, perform the following steps.
-  Choose an arbitrary element in the array and call it pivot. 
-  Move the elements around in the array so that two groups are formed. The element pivot should be placed between the two groups. All the elements that are less than or equal to pivot should be placed in the group to the left of the pivot and all the rest in the group to the right. 
- Sort the part of the array to the left of pivot using the algorithm
- Sort the part of the array to the right of pivot using the algorithm

### Time complexity

- Best case: $O(Nlog_2N)$
- Average case: $O(Nlog2N)$
- Worse case: $O(N^2)$
- If the list is completely or almost ordered, it can take a running time of order $N^2$.



# Merge Sort

```python
def mergesort(arr):
    # splitting
    if len(arr) <= 1:
        return arr
    midpt = len(arr) // 2
    left = arr[:midpt]
    right = arr[midpt:]

    left = mergesort(left)
    right = mergesort(right)

    ms = []
    lidx = 0
    ridx = 0

    while lidx < len(left) and ridx < len(right):
        if left[lidx] < right[ridx]:
            ms.append(left[lidx])
            lidx += 1
        else:
            ms.append(right[ridx])
            ridx += 1
    
    while lidx < len(left):
        ms.append(left[lidx])
        lidx += 1

    while ridx < len(right):
        ms.append(right[ridx])
        ridx += 1

    return ms # return ms
```

### Method

- If there is only 1 element in the list it is already sorted, return.
- Divide the list recursively into 2 halves until it can no longer be divided. 
- Merge the smallest list into a new list in sorted order. 


### Time Complexity

Worst Case Time: $O(Nlog_2N)$
Best Case Time: $O(Nlog_2N)$
Average Time: $O(Nlog_2N)$

Not recommended for large unsorted arrays as it requires equal amount of additional space as the unsorted array. 




# In place v.s. Not in place

  

##### In-place sort

- Performed when the number of elements is small enough to fit into the main memory. 
- To produce the desired output, modification to the data set only requires only small and constant extra space.     
- E.g.
	- Insertion sort, bubble sort, quick sort
    

##### Not-In-place sort

- When all elements that needs to be sorted cannot be placed in memory at a time, therefore additional memory is required to perform the sorting
- E.g.
	- Merge sort





>[!Comparison]
>- Bubble sort does perform better for partially sorted lists because it is able to detect when a list is sorted and does not continue making unnecessary passes through the list. As a general sorting scheme, however, it is very inefficient because of the large number of interchanges that it requires. In fact, it is the least efficient of the sorting schemes. 
>- Insertion sort also is too inefficient to be used as a general-purpose sorting scheme. However, the low overhead that it requires makes it better than bubble sort. 
>- While Quick sort partitions and usually makes less comparisons than Bubble sort and Insertion sort, in the worst case scenario the time complexity is still $O(n^2)$. 
>- Merge sort has a time complexity of $O(nlog_n)$ and is a very efficient general-purpose sorting schemes and especially for large lists.
