---
tags:
  - data-structure
  - tree
  - practical
---
# Definition

- A hierarchical data structure consisting of nodes.
- Each node is linked to one or more nodes below it.

# Common terms:

- `Root `– the topmost node.
- Subtree – a tree formed from any node and its descendants.
- Node – an individual element in the tree.
- Leaf (Terminal) Node – a node with no children.

# Tree Traversals

### Preorder (Root → Left → Right)

- Visit the `root`
 - Traverse the `left` subtree.
- Traverse the `right` subtree.

### Inorder (Left → Root → Right)

- Traverse the `left `subtree.
- Visit the `root`.
- Traverse the `right` subtree.

>[!Note]
>For a Binary Search Tree (BST), this traversal visits nodes in ascending order.

### Postorder (Left → Right → Root)

- Traverse the `left` subtree.
- Traverse the `right` subtree.
- Visit the `root`.

### Binary Search Tree (BST) Creation

- Accept the `data`.
- If the `data` is invalid, stop.
- Start from the `root` pointer.
- If the tree is empty, insert the data as the root node.
- Otherwise:
	- If `data < current node`, move to the left subtree.
	- Else, move to the `right `subtree.
	- Repeat until an empty position is found and insert the node.

### Binary Search Tree (BST) Search

- Accept the data to search.
- Start from the root.
- While the current node is not NULL:
	- If `data == current node`, print "Found" and stop.
	- If `data < current node`, move to the left subtree.
- Else, move to the right subtree.
- If `NULL` is reached, print "Not Found".



# Code

### 1st version


```python
class Node:
    def __init__(self,data):
        self.left = None
        self.right = None
        self.data = data

    def insert(self,data):
        if data < self.data:
            if not self.left:
                self.left = Node(data)
            else:
                self.left.insert(data)
        else:
            if not self.right:
                self.right = Node(data)
            else:
                self.right.insert(data)
    
    def search(self,value):
        if value == self.data:
            return True
        elif value < self.data:
            if self.left:
                return self.left.search(value)
            else:
                return False
        else:
            if self.right:
                return self.right.search(value)
            else:
                return False
    
    def inOrder(self):
        if self.left:
            self.left.inOrder()
        print(self.data)       
        if self.right:
            self.right.inOrder()
```



### 2nd version


```python
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None
    
class BST:
    def __init__(self):
        self.root = None
    
    def insert(self, value, node=None):
        if self.root == None:
            self.root = Node(value)
        if node == None:
            node = self.root
        if node.data < value:
            if node.right:
                self.insert(value, node=node.right)
            else:
                node.right = Node(value)
        elif node.data > value:
            if node.left:
                self.insert(value, node=node.left)
            else:
                node.left = Node(value)
    
    def search(self, value, node=None):
        if self.root == None:
            self.root = Node(value)
        if node == None:
            node = self.root
        if node.data == value:
            return True
        elif node.data < value:
            if node.right:
                return self.search(value, node=node.right)
            else:
                return False
        elif node.data > value:
            if node.left:
                return self.search(value, node=node.left)
            else:
                return False

    def inOrder(self, node=None):
        if node == None:
            node = self.root
        if node.left:
            self.inOrder(node.left)
        print(node.data)
        if node.right:
            self.inOrder(node.right)

```



### 3rd version


```python
class Node:
    def __init__(self,data):
        self.data = data
        self.right = None
        self.left = None
    
def insert(root, value):
    if root == None:
        return Node(value)
    elif root.data > value:
        root.left = insert(root.left, value)
    elif root.data < value:
        root.right = insert(root.right, value)
    return root


def search(root, value):
    if root.data == value:
        return True
    elif root.data > value:
        if root.left:
            return search(root.left, value)
        else:
            return False
    elif root.data < value:
        if root.right:
            return search(root.right, value)
        else:
            return False
        

def inOrder(root):
    if root.left:
        inOrder(root.left)
    print(root.data)
    if root.right:
        inOrder(root.right)
```


