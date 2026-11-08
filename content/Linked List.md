---
tags:
  - linked-list
  - data-structure
  - practical
---
# Definition

- A linked list is a dynamic data structure consisting of nodes.
- Each node contains:
	- Data.
	- Pointer to the next node.

# Deleting a Node

- Find the previous node.
- Update the previous node's next pointer.
- Free the deleted node.
### Special Cases:

- Empty list.
- First and only node.
- First node.
- Middle node.
- Last node.

# Free Space List

### Definition

- Stores unused nodes.
- The free pointer points to the first available node.

### Ordered Insertion

1. **Create a new node** containing the value to be inserted.
2. If the linked list is **empty**, **set the new node as the head**.
3. Otherwise, **compare** the new value with the head node:
   - If the new value is **less than** the head node's value, **insert the new node before the head** and **update the head pointer**.
   - Otherwise, **start traversing from the head**.
4. **Traverse the linked list** and compare the new value with the next node's value:
   - If the new value is **greater than or equal to** the next node's value, **move to the next node**.
   - Otherwise, **stop traversing**.
5. **Repeat step 4** until the **correct position is found** or the **end of the list is reached**.
6. **Update the pointers**:
   - Set the **new node's next pointer** to the current node's next node.
   - Set the **current node's next pointer** to the new node.

### Insertion at the back

1. **Create a new node** containing the value to be inserted and **set its next pointer to null**.
2. If the linked list is **empty**, **set the new node as the head**.
3. Otherwise, **start traversing from the head node**.
4. **Move to the next node** repeatedly until the **last node** is reached (its next pointer is null).
5. **Set the last node's next pointer to the new node**, inserting it at the end of the linked list.

### Deletion

- Search for the node.
- Remove it from the linked list.
- Link it to the front of the free list.
- Update the free pointer.





