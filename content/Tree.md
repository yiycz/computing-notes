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





