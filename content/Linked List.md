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

- Traverse the linked list to find the correct insertion position.
	- Compare the new data with existing nodes.
	- Stop when you find the first node whose value is greater than the new data.
	- Keep track of both the current node and the previous node.
- Check whether there is a free node available.
	- If the free pointer is `NULL`, the free list is empty and insertion cannot proceed (memory overflow).
	- Otherwise, continue.
- Remove the first node from the free list.
	- Let the node pointed to by free become the new node.
	- Update the free pointer to point to the next available free node.
- Store the new data in the allocated node.
	- Copy the value to be inserted into the node's data field.
- Insert the node into the linked list.
	- If inserting at the beginning, make the new node point to the current head, then update the head pointer.
	- Otherwise:
		- Set the new node's next pointer to the current node.
- Update the previous node's next pointer to point to the new node.
	- Update the free pointer.
- The free pointer should already point to the next available free node after allocation.

### Deletion

- Search for the node.
- Remove it from the linked list.
- Link it to the front of the free list.
- Update the free pointer.



# Code

```python
class Node:
    def __init__(self,data):
        self.next = None
        self.data = data


class linkedList:
    def __init__(self):
        self.root = None


    def insertToHead(self, value):
        if self.root == None:
            self.root = Node(value)
        else:
            newNode = Node(value)
            newNode.next = self.root
            self.root = newNode


    def insertToEnd(self, value):
        if self.root == None:
            self.root = Node(value)
        else:
            curr = self.root 
            while curr.next != None:
                curr = curr.next
            curr.next = Node(value)
    

    def deleteFromBack(self):
        if self.root == None:
            return False
        elif self.root.next == None:
            self.root == None
        else:
            curr = self.root
            while curr.next.next != None:
                curr = curr.next
            curr.next = None
    
    def deleteFromFront(self):
        if self.root == None:
            return False
        elif self.root.next == None:
            self.root == None
        else:
            self.root = self.root.next

    def deleteByValue(self, value):
        if self.root == None:
            return False
        elif self.root.next == None and self.root.next.data == value:
            self.root == None
        elif self.root.next == None and self.root.next.data != value:
            return False
        else:
            prev = None
            curr = self.root
            while curr.next != None and curr.data != value:
                prev = curr
                curr = curr.next
            if curr.data == value:
                prev.next = curr.next
            else:
                return False

    def display(self):
        if self.root == None:
            return
        else:
            array = []
            curr = self.root
            while curr != None:
                array.append(curr.data)
                curr = curr.next
            print(array)
```

