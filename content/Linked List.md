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

### Ordered Insertion (Linked List)

1. **Create** a new node containing the value to be inserted.
2. **Check the head**:
   - If the list is **empty**, set the new node as the **head**.
   - If the new value is **less than** the head's value, **insert before the head** and **update the head pointer**.
3. **Traverse** from the head, moving to the **next node** while its value is **less than or equal to** the new value, until the **correct position** or **end of the list** is reached.
4. **Update the pointers**:
   - Set the **new node's next pointer** to the **current node's next node**.
   - Set the **current node's next pointer** to the **new node**.

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





