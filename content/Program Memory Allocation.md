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

- Flexible size
	- Can grow or shrink during program execution. No need to know the size beforehand.

- Better memory utilisation
	- Memory is allocated only when needed, reducing wasted space.

# Disadvantages of using dynamic ds over static ds

- More memory overhead
	- Slower access

- Many dynamic structures (e.g., linked lists) do not support direct indexing, so elements may need to be traversed one by one.
