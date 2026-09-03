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

```python
class Stack:  

def __init__(self, max_size):  
	self.__max_size = max_size  
	self.__stack_ptr = -1  
	self.__container = [None for i in range(max_size)]  
  
def isEmpty(self):  
	return self.__stack_ptr == -1  
  
def isFull(self):  
	return self.__stack_ptr == self.__max_size - 1  
  
def size(self):  
	return self.__stack_ptr + 1  
  
def peek(self):  
	return self.__container[self.__stack_ptr]  
  
def push(self, val):  
	if self.isFull():  
		print(f"The stack is full. Terminating push({val}).")  
	return  
	self.__stack_ptr += 1  
	self.__container[self.__stack_ptr] = val  
  
def pop(self):  
	if self.isEmpty():  
	print(f"The stack is empty. Terminating pop().")  
	return  
	  
	popped_val = self.peek()  
	self.__container[self.__stack_ptr] = None  
	self.__stack_ptr -= 1  
	return popped_val
```