---
tags:
  - data-structure
---
# Code Segment (CS) or Text Segment

### Purpose

- Stores all the executable instructions (machine code) of the program
- This includes:
	- Complied code of functions and methods
	- Constants such as string literals in some systems

### Memory Characteristics:

- Fixed Size – determined at compile time (cannot change at runtime)
- Read-only – prevents accidental modification of program instructions, ensuring integrity and security
- Lowest memory address – typically the first segment loaded into memory

>[!Additional Notes:]
>
> - Shared among multiple instances of the same program to save memory
> - Attempts to modify code here will cause a segmentation fault (RTE)


# Data Segment (DS) / Initialised Data

### Purpose:

- Stores all global and static variables that have been explicitly initialised before execution begins.

### Memory Characteristics:

- Fixed Size – determined at compile time
- Read/Write – values can be modified during program execution

>[!Additional Notes:]
>
>- Retains values between function calls (for static variables)
>- Occupies space throughout the program’s lifetime



# BSS (Block Started by Symbol)

### Purpose:

- Stores global and static variables that are declared but not initialised (uninitialised data).

### Memory Characteristics:

- Fixed Size – determined at compile time
- Read/Write access
- Initialised to zero (0) by default before program execution begins.

>[!Additional Notes:]
>
>- Does not occupy space in the executable file (only reserved during runtime)
>- Help reduce program file size


# Heap / Extra Segment (ES)

### Purpose:

- Used for dynamic memory allocation during program execution (runtime)

### Memory Characteristics:

- Grows upward (towards higher memory addresses)
- Variable Size – expands and contracts as memory is allocated or freed (malloc, free, new, delete)
- Read/Write access

>[!Additional Notes:]
>
>- Shared by all threads, shared libraries, and dynamically loaded modules in a process
>- Memory must be managed by the programmer (risk of memory leaks or fragmentation)
>- Heap corruption or overflow can cause program crashes.

### Stack Segment (SS)

### Purpose:

- Used for function call management and storing temporary variables
- Includes:
	- Function parameters
	- Return addresses
	- Local variables

### Memory Characteristics:

- Grows downwards (toward lower memory addresses)
- Variable Size
- LIFO Structure (Last In, First Out)
- Read/Write access

>[!Additional Notes:]
>
>- Each thread has its own independent stack
>- Managed automatically by the operating system
>- Exceeding the stack size limit leads to a stack overflow error (e.g. infinite recursion)

# Advantage of using dynamic ds over static ds

- **No fixed size limitation**: Dynamic data structures can **grow as needed** without a **predetermined maximum size**, unlike static arrays. Dynamic linked lists can accommodate as many elements as needed, limited only by **available system memory**.

- **No wasted space**: Dynamic data structures **allocate memory only for elements stored at runtime**. In contrast, static arrays **reserve a fixed amount of memory** even when some elements are unused, resulting in **wasted memory space**.

# Disadvantages of using dynamic ds over static ds

- **Faster access**: Static arrays allow **direct access to elements using their indices**, making data retrieval faster than in dynamic linked lists, which require **sequential traversal** to access a specific element.

- **Lower memory overhead**: Static arrays do not require **additional memory to store pointers** between elements. In contrast, dynamic linked lists require **extra memory for pointers** in each node.

- **Simpler memory management**: Static arrays allocate a **fixed amount of memory** at the start, eliminating the need for **dynamic memory allocation and deallocation** during runtime.
