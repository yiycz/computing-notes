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


Insertion sort is an **in-place sorting algorithm** that builds a **sorted portion of the array** by repeatedly **inserting each element into its correct position**.

It starts by **considering the first element as sorted**. The next element is selected and **compared with elements in the sorted portion**, moving from right to left.

**Elements greater than the selected element are shifted one position to the right** to make space for its insertion. This process is **repeated until all elements have been inserted into their correct positions**, resulting in a fully sorted array.


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


Quick sort is a **divide-and-conquer algorithm** that recursively partitions an array around a **pivot element**, sorts the resulting subarrays, and produces a single sorted array.

It starts by **selecting a pivot element** and **partitioning the array**, such that elements smaller than the pivot are placed on its left and elements greater than the pivot are placed on its right.

The process is **repeated recursively** on the resulting subarrays until each subarray contains **zero or one element**, which is considered sorted. The entire array is then sorted **without requiring a separate merging process**.


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


Merge sort is a **divide-and-conquer algorithm** that recursively **splits an array into halves**, sorts each half, and **merges the sorted halves** into a single sorted array.

It starts by **dividing the input array into halves repeatedly**, until each subarray contains **only one element**. Each subarray with one element is considered as sorted.

**Sorted sub-arrays are then merged**, such that the merged results **remain sorted throughout the process**.



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





# Comparison between sorts


# Sorting Algorithms Comparison

## Overview

| Algorithm | Best Time | Average Time | Worst Time | Auxiliary Space | Stable |
|---|---|---|---|---|---|
| Bubble Sort | O(n) | O(n²) | O(n²) | O(1) | Yes |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes |
| Quick Sort | O(n log n) | O(n log n) | O(n²) | O(log n) average | No |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | Yes |

Note: Bubble sort's O(n) best case assumes early termination optimisation. Merge sort and quick sort figures refer to standard array implementations.

## 1. Bubble Sort vs Merge Sort

- **Less memory required**: Bubble sort is an **in-place sorting algorithm** (sorts within the original array), while merge sort requires the **creation of temporary sub-arrays** in the process and there is **recursive call stack overhead**, which can be an issue for **large arrays or memory-constrained systems**.

- **Possible early termination**: For bubble sort, if **no swaps were made during a pass**, the algorithm **terminates early**, making it efficient for **nearly-sorted data**. In contrast, merge sort always performs the **full divide-and-conquer process** regardless of the initial order, making it less efficient for nearly-sorted cases.

- **Faster for large datasets**: Merge sort has a **time complexity of O(n log n)** in all cases, while bubble sort has an **average and worst-case time complexity of O(n²)**. Hence, merge sort is generally more efficient for **large datasets**.

- **More predictable performance**: Merge sort consistently performs in **O(n log n) time**, regardless of the initial arrangement of elements. In contrast, bubble sort's performance depends on the **initial order of elements**.

## 2. Bubble Sort vs Quick Sort

- **Faster for large datasets**: Quick sort has an **average time complexity of O(n log n)**, while bubble sort has an **average time complexity of O(n²)**. Hence, quick sort is generally more efficient when sorting **large datasets**.

- **Less memory required**: Bubble sort requires only **O(1) auxiliary space** as it sorts elements in-place without recursion. In contrast, quick sort requires **O(log n) stack space on average** for recursive calls.

- **Stable sorting**: Bubble sort is a **stable sorting algorithm**, preserving the **relative order of elements with equal values**. In contrast, standard quick sort is **unstable**, as partitioning may change their relative order.

- **Possible early termination**: Optimised bubble sort can **terminate early if no swaps are made during a pass**, achieving **O(n) time** for an already sorted array. In contrast, standard quick sort continues **partitioning the array recursively**, typically requiring **O(n log n) time** with balanced partitions, or **O(n²)** with highly unbalanced partitions.

- **Worst-case performance**: Both bubble sort and quick sort have a **worst-case time complexity of O(n²)**. However, quick sort only reaches this worst case when **highly unbalanced partitions** are repeatedly produced, whereas bubble sort performs O(n²) comparisons on average.

## 3. Bubble Sort vs Insertion Sort

- **Faster for nearly-sorted data**: Insertion sort is generally more efficient for **nearly-sorted arrays**, as it only needs to **shift a small number of elements** into their correct positions. In contrast, bubble sort may require **multiple passes and adjacent swaps** to move elements into their correct positions.

- **Fewer data movements**: Insertion sort typically **shifts elements** to make space for the element being inserted, reducing unnecessary data movements. In contrast, bubble sort repeatedly **swaps adjacent elements** that are in the wrong order.

- **Efficient for incremental sorting**: Insertion sort can **insert new elements into an already sorted portion** without sorting the entire array again. In contrast, bubble sort generally requires **repeated passes through the array** to restore the correct order.

- **Similar memory requirements**: Both bubble sort and insertion sort are **in-place sorting algorithms** requiring only **O(1) auxiliary space**, making them suitable for **memory-constrained systems**.

- **Stable sorting**: Both bubble sort and insertion sort are **stable sorting algorithms**, preserving the **relative order of elements with equal values**.

## 4. Merge Sort vs Quick Sort

- **More predictable performance**: Merge sort guarantees a **time complexity of O(n log n)** in all cases. In contrast, quick sort has an **average time complexity of O(n log n)** but may degrade to **O(n²)** when repeatedly choosing poor pivots.

- **Less memory required**: Quick sort typically sorts elements **in-place**, requiring only **O(log n) stack space on average** for recursive calls. In contrast, merge sort requires **O(n) auxiliary space** for temporary arrays, making quick sort more memory-efficient for array sorting.

- **Stable sorting**: Merge sort is a **stable sorting algorithm**, preserving the **relative order of elements with equal values**. In contrast, standard quick sort is **unstable**, as partitioning may change their relative order.

- **Better cache performance**: Quick sort generally exhibits **good cache locality** as it partitions and sorts elements within the original array. In contrast, standard merge sort requires **temporary arrays and additional copying**, which can introduce memory overhead.

- **Different divide-and-conquer approaches**: Merge sort **divides the array into halves**, recursively sorts them and **merges the sorted sub-arrays**. In contrast, quick sort **partitions the array around a pivot** before recursively sorting the partitions.

## 5. Merge Sort vs Insertion Sort

- **Faster for large datasets**: Merge sort has a **time complexity of O(n log n)** in all cases, while insertion sort has an **average and worst-case time complexity of O(n²)**. Hence, merge sort is generally more efficient for **large datasets**.

- **Less memory required**: Insertion sort is an **in-place sorting algorithm** requiring only **O(1) auxiliary space**. In contrast, merge sort requires **O(n) auxiliary space** for temporary arrays, making insertion sort more suitable for **memory-constrained systems**.

- **Faster for nearly-sorted data**: Insertion sort can achieve **O(n) time** when the array is already sorted and performs efficiently when **few elements are out of order**. In contrast, merge sort requires **O(n log n) time** regardless of the initial arrangement of elements.

- **Better for small datasets**: Insertion sort has **low algorithmic overhead** as it does not require recursion or temporary arrays. In contrast, merge sort involves **recursive splitting and merging**, making insertion sort often faster for **small datasets**.

- **Stable sorting**: Both merge sort and insertion sort are **stable sorting algorithms**, preserving the **relative order of elements with equal values**.

## 6. Quick Sort vs Insertion Sort

- **Faster for large datasets**: Quick sort has an **average time complexity of O(n log n)**, while insertion sort has an **average time complexity of O(n²)**. Hence, quick sort is generally more efficient for **large datasets**.

- **Less memory required**: Insertion sort is an **in-place sorting algorithm** requiring only **O(1) auxiliary space**. In contrast, quick sort requires **O(log n) stack space on average** for recursive calls.

- **Faster for nearly-sorted data**: Insertion sort is efficient for **nearly-sorted arrays**, achieving **O(n) time** for already sorted data. In contrast, quick sort continues **partitioning the array recursively**, typically requiring **O(n log n) time** with balanced partitions.

- **Stable sorting**: Insertion sort is a **stable sorting algorithm**, preserving the **relative order of elements with equal values**. In contrast, standard quick sort is **unstable**, as partitioning may change their relative order.

- **Better for small datasets**: Insertion sort has **low algorithmic overhead** and does not require **recursive calls or pivot selection**, making it efficient for **small datasets**. In contrast, quick sort involves **partitioning and recursive calls**, which can introduce additional overhead.

- **Worst-case performance**: Both insertion sort and quick sort have a **worst-case time complexity of O(n²)**. However, insertion sort performs efficiently on **already sorted data**, while quick sort's performance depends on **pivot selection and partition balance**.

