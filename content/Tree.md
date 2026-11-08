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

### BST Insertion
1. **Create a new node** containing the value to be inserted.
2. If the BST is **empty**, **set the new node as the root**.
3. Otherwise, **start from the root node** and **compare** the new value with the current node:
   - If the new value is **less than** the current node's value, **move to the left child**.
   - If the new value is **greater than** the current node's value, **move to the right child**.
   - If the values are **equal**, handle the duplicate according to the BST's rules.
4. **Repeat step 3** until an **empty child position** is found.
5. **Insert the new node** at that position, maintaining the **BST property**.

### BST Search
1. **Start from the root node**.
2. **Compare** the target value with the current node's value:
   - If the target **matches** the current node's value, **return the node** (search successful).
   - If the target is **less than** the current node's value, **move to the left child**.
   - If the target is **greater than** the current node's value, **move to the right child**.
3. **Repeat step 2** until the target is **found** or a **null node** is reached (target not found in BST).






