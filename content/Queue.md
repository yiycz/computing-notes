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

