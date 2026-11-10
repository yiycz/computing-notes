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
>[!answer]
>- Each time a recursive function is called, a new stack frame, containing function's local variables, parameters, and the return address (the point to return to after the function finishes execution), is created. 
>- The newly created stack frame is pushed onto the calls stack. This means that the execution context of the current function call is saved at the top of the stack. The stack grows with each recursive call.
>- The execution of the current function is suspended. The new function call is executed with its own stack frame at the top of the stack. 
>- When a base case is reached or the function completes its task, the function returns a value. The current stack frame is then popped from the stack , and the execution resumes from the return address saved in the stack frame of the previous function call. The process continues until all recursive calls are resolved and the stack is empty again.

