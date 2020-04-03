# Trees

## Common Terminology

- _Node_: The individual object that holds data within a tree structure.  
- _Root_: The first or top Node in a tree.  
- _Left Child_: The node that is positioned to the left of a root or node.  
- _Right Child_: The node that is positioned to the right of a root or node.  
- _Edge_: The link between a parent and child node.  
- _Leaf_: A node that does not contain any children nodes.
- _Height_: The number of Edges from the root to the botommost leaf.

## Traversal Through A Tree

There are two types of traversal through trees:
- Depth First
- Breadth First

#### Depth First

Depth first traversal is moving through the tree by its height before its breadth.

#### Breadth First

Breadth first traversal iterates through our tree node by node on each level.

## Binary Trees

Typically speaking, a tree can have any number of children per node, but a Binary Tree can only have two children per node.

Binary trees have no established rules on where to add nodes in the tree, which means that they can be in any order. Common convention is to use a queue to add new nodes in a breadth traversal fashion.

_Link to source document [here](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)._
