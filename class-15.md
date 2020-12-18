# Explore the Tech!

## 1. Binary Tree:

##### Terminology:
* `Node` - A node is the individual item/data that makes up the data structure.
* `Root` - The root is the first/top Node in the tree.
* `Left Child` - The node that is positioned to the left of a root or node.
* `Right Child` - The node that is positioned to the right of a root or node.
* `Edge` - The edge in a tree is the link between a parent and child node.
* `Leaf` - A leaf is a node that does not contain any children.
* `Height` - The height of a tree is determined by the number of edges from the root to the bottommost node.

##### Traversals:
1. Depth-First-Search.
  Pre-order: `root >> left >> right`
  In-order: `left >> root >> right`
  Post-order: `left >> right >> root`
2. Breadth-First Search.
  Iterates through the tree by going through each level of the tree node-by-node.
  

> Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).

##### Adding a node:
One strategy for adding a new node to a binary tree is to fill all “child” spots from the top down. To do so, we would leverage the use of breadth first traversal. 
During the traversal, we find the first node that does not have 2 child nodes, and insert the new node as a child. We fill the child slots from left to right.


## 2. Binary Search Trees
A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. 
In a BST, nodes are organized in a manner where all values that are smaller than the root are placed to the left, 
and all values that are larger than the root are placed to the right.

##### Searching a BST:
Example: 
Let’s say we are searching `15` in a tree. We start by comparing the value 15 to the value of the root, `23`.

`15 < 23`, so we traverse the left side of the tree. We then treat 8 as our new “root” to compare against.

`15 > 8`, so we traverse the right side. 16 is our new root.

`15 < 16`, so we traverse the left side. And aha! 15 is our new root and also a match with what we were searching for.
