---
tags:
  - data-structure
---

# Advantage of using dynamic ds over static ds

- **No fixed size limitation**: Dynamic data structures can **grow as needed** without a **predetermined maximum size**, unlike static arrays. Dynamic linked lists can accommodate as many elements as needed, limited only by **available system memory**.

- **No wasted space**: Dynamic data structures **allocate memory only for elements stored at runtime**. In contrast, static arrays **reserve a fixed amount of memory** even when some elements are unused, resulting in **wasted memory space**.

# Disadvantages of using dynamic ds over static ds

- **Faster access**: Static arrays allow **direct access to elements using their indices**, making data retrieval faster than in dynamic linked lists, which require **sequential traversal** to access a specific element.

- **Lower memory overhead**: Static arrays do not require **additional memory to store pointers** between elements. In contrast, dynamic linked lists require **extra memory for pointers** in each node.

- **Memory fragmentation**. This occurs when **lots of small pockets of memory** are **allocated** in the host system’s memory, such that there are **no contiguous blocks of free memory** large enough for any process that requires it. So the computer runs out of memory for other processes. [In contrast, static data structures that use **contiguous blocks of memory**] 

