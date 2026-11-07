---
tags:
  - data-structure
  - stack
  - practical
---
# Definition

A stack is a linear data structure that stores elements in a Last In, First Out (LIFO) order, meaning the last element added (pushed) is the first one removed (popped).


# Characteristics of a Stack

- Order: Last In, First Out (LIFO)
- Access: Only the top element is directly accessable
- Dynamic Size: Can grow or shrink as elements are pushed or popped
 - Restricted Operations: Unlike arrays/lists, you can’t directly access elements by index directly
- Implementation: Can be implemented using arrays (static stack) or linked lists (dynamic stack)

# Core Operations

`push(x)` – adds element x at the top of the stack
`pop()` – removes and returns the element from the top of the stack
`peek() or top() `– returns the topmost element without removing it
`isEmpty()` – checks whether the stack is empty
`isFull()` – (for fixed stacks) checks if the stack has reached its max size

