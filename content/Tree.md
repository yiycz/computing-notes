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
1. **Create**: Create a **new node** containing the value to be inserted. If the BST is **empty**, set the new node as the **root**.
2. **Compare**: Starting from the **root**, compare the new value with the current node's value:
   - If **smaller**, move to the **left child**.
   - If **greater**, move to the **right child**.
   - If **equal**, handle the duplicate according to the BST's rules.
3. **Repeat**: Continue comparing and traversing until an **empty child position** is found.
4. **Insert**: Insert the **new node** at that position, maintaining the **BST property**.

### BST Search
1. **Start**: Begin at the **root node**.
2. **Compare**: Compare the target value with the current node's value:
   - If **equal**, the target is **found**.
   - If **smaller**, move to the **left child**.
   - If **greater**, move to the **right child**.
3. **Repeat**: Continue comparing and traversing until the **target is found** or a **null node is reached**, indicating that the target is not in the BST.






