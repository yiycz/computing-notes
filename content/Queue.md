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


1. **Create a new item** containing the data and its priority.
2. If the priority queue is **empty**, **insert the new item at the front**.
3. Otherwise, **traverse the priority queue from the front** and **compare priorities**:
   - If the new item has a **higher priority**, **insert it before the current item**.
   - If the new item has an **equal priority**, **continue traversing** to preserve FIFO order among items with the same priority.
   - If the new item has a **lower priority**, **move to the next item**.
4. **Repeat step 3** until the **correct position is found** or the **end of the queue is reached**.
5. **Insert the new item at that position**, maintaining the **priority order**.



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

