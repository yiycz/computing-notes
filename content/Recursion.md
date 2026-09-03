---
tags:
  - recursion
  - theory
---
# Definition

- A recursive function is a function that calls itself (#1).
- The recursive function must have a base case (#2), 
- and it must change its state and move toward the base case (#3).

>[!note]
>  Must include all three points when explaining recursion.


# How recursion is handled in memory

- Function calls use the stack:
	- Every time a function is called (recursive or not), a stack frame (activation record) is created on the stack segment of memory.
	- The stack frame stores:
		- Function parameters
		- Local variables
		- Return addresses
		- Possibly saved CPU registers and bookkeeping information

- Each recursive call creates a new stack frame:
	- When a recursive function calls itself, a new copy of its stack frame is pushed onto the stack
	- Each frame is independent, even though it’s the same function → each one has its own local variables and parameters

- Base case terminates recursion:
	- When the base case is reached, the function returns a value instead of making another recursive call.
	- This value is returned to the caller’s stack frame (the one just below it on the stack)

- Stack unwinding:
	- As each recursive call finishes, its stack frame is popped off the stack
	- Control returns to the previous frame, which can now continue execution
	- This continues until the initial call’s frame (in main()) is reached.

- Notes:
	- Every recursive call consumes some stack memory for its frame
	- If recursion is too deep (e.g. missing base case or very large input), the stack can fill up, causing a stack overflow error.

### Order in which items are pushed onto each stack frame

- Function Arguments (pushed by the caller)
- Return address (pushed by the CPU automatically)
- Previous EBP/RBP value (pushed by the callee)
- Local Variables (pushed by the callee)

C++
```c++
int Add(int a, int b) {  
	int sum = a + b;  
	return sum;  
}  

int main() {  
	int result = Add(2, 3);  
}
```

Assembly:
```js
main:
      push 3		; Step 1a: push second argument (b), right to left
      push 2		; Step 1b: push first argument (a)
      call Add	; Step 2: CPU pushes return address automatically, then jumps to add function

Add:
	push ebp	; Step 3a: Save caller's EBP
	mov ebp, esp	; Step 3b: Set up new EBP (frame pointer)
	sub esp, 4	; Step 4a: Reserve 4 bytes for local variable "sum"
	mov eax, [ebp+8]	; load a into eax
	add eax, [ebp+12]	; eax = a + b
	mov [ebp-4], eax	; store the result in sum
	mov eax, [ebp-4] 	; return value into eax
	mov esp, ebp		; deallocate local variables
	pop ebp		; restore caller's EBP
	ret			; pop return address and jump back
```


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

