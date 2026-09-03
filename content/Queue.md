---
tags:
  - data-structure
  - practical
  - queue
---
# Linear Queue

### Definition

- A FIFO (First In, First Out) data structure.
- Insertion occurs at the rear.
- Deletion occurs at the front.

### Pointers

- Front Pointer (FP).
- Rear Pointer (RP).

### Operations

`Enqueue()`
- Increment RP.
- Insert a new element.
- Overflow occurs when the queue is full.

`Dequeue()`
- Remove the front element.
- Increment FP.
- Underflow occurs when attempting to remove from an empty queue.
- Queue is empty when:
	- FP == -1
	- FP > RP

### Disadvantage

Freed spaces at the front cannot be reused once RP reaches the end.


# Circular Queue

```python
class c_queue:
    def __init__(self):
        self.size = 6
        self.array = [None for _ in range(self.size)]
        self.fp = -1
        self.rp = -1


    def isFull(self):
        return (self.rp + 1) % self.size == self.fp


    def isEmpty(self):
        return self.fp == -1

    def enqueue(self, item):
        if self.isFull():
            return "FULL"
        else:
            if self.fp == -1:
                self.fp = 0
            self.rp = (self.rp + 1) % self.size
            self.array[self.rp] = item

    def dequeue(self):
        if self.isEmpty():
            return "Empty"
        else:
            value = self.array[self.fp]
            if self.fp == self.rp:
                self.fp = -1
                self.rp = -1
            else:
                self.fp = (self.fp + 1) % self.size
            return value 

    def display(self):
        print(self.array)
```

### Definition

- Treats the array as circular.
- Next position: `(pointer + 1) % maxsize`

### Conditions

`isFull()`
- `(rp + 1) % maxsize == fp`

`isEmpty()`
- `fp == -1`

### Advantages

- Reuses empty spaces.
- Better memory utilisation.
- Supports continuous insertion and deletion.
- Maintains FIFO order.

# Priority Queue (Heap)

### Definition

- Removes elements according to priority rather than insertion order.

### Insertion (Bubble Up)

- Insert the new element at the last available position in the heap to maintain the complete binary tree property.
- Compare the new element with its parent node.
- If the heap property is violated, swap the new element with its parent.
- Max Heap: Swap while the new element is greater than its parent.
- Min Heap: Swap while the new element is smaller than its parent.
- Repeat the comparison and swapping until the heap property is restored or the root is reached.

### Deletion (Bubble Down)

- Remove the root.
- Replace it with the last element.
- Compared with the children.
- Swap until the heap property is restored.

# Applications of Queues

- Printer queues.
- CPU scheduling.
- Keyboard buffering.
- Network packet buffering.
- Breadth-First Search (BFS).
- Producer-consumer systems.
- I/O buffering between CPU and peripherals.

