---
tags:
  - recursion
  - theory
---

# Definition
- A recursive function is a function that calls itself (#1).
- The recursive function must have a base case (#2), 
- and it must change its state and move toward the base case (#3).

# Advantages of Recursion:
- Sometimes, recursive solutions are shorter than non-recursive ones
- When the solution to be problem is essentially recursive (e.g. DFS)
    

# Disadvantages of Recursion:
- May require large amounts of memory if the depth of recursion if large
	- Could result in stack overflow, causing the program to crash
	- Memory overheads of stack use with many recursive procedural calls
- Recursive routines are sometimes very slow in execution owing to the overheads in memory involved in repeatedly calling the subroutine and storing and retrieving return addresses and parameters
- Recursive routines can be difficult to follow and to debug


# Explain Recursion Using Stack

- Each function call **creates a stack frame/activation record** on the call stack.
- The frame stores items such as **parameters, local variables and the return address.**
- A recursive call **pushes a new frame**; earlier calls remain **suspended.**
- When **a base case reached**, frames are popped in **LIFO order** and return **values/control** pass back through the **earlier calls**.

