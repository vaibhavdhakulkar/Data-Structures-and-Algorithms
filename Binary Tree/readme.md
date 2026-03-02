# Binary Tree
A binary tree is a hierarchical data structure where each node has at most two children, referred to as the left child and the right child.

Structure of a Node
Each node contains:
- Data – the value stored
- Left pointer – points to the left child
- Right pointer – points to the right child

        [Data]
       /       \
  [Left]     [Right]

## Key Terminology
TermMeaningRootThe topmost node (no parent)LeafA node with no childrenParentA node that has childrenChildA node descended from anotherHeightLongest path from root to a leafDepthDistance of a node from the rootSubtreeA node and all its descendantsLevelGeneration of nodes (root = level 0)

## Example
            10          ← Root (Level 0)
           /  \
          5    20       ← Level 1
         / \   / \
        3   7 15  25   ← Level 2 (Leaves)

## Types of Binary Trees
1. Full Binary Tree
- Every node has 0 or 2 children (never just 1).
        1
       / \
      2   3
     / \
    4   5
  <br>
2. Complete Binary Tree
- All levels are fully filled except possibly the last, which is filled left to right.
        1
       / \
      2   3
     / \ /
    4  5 6
  <br>
3. Perfect Binary Tree
- All internal nodes have 2 children and all leaves are at the same level.
        1
       / \
      2   3
     / \ / \
    4  5 6  7
  <br>
4. Degenerate (Skewed) Tree
- Every parent has only one child — essentially a linked list.
    1
     \
      2
       \
        3
         \
          4
<br>
5. Balanced Binary Tree
- The height of left and right subtrees of every node differs by at most 1. (e.g., AVL Tree)
<br>

6. Binary Search Tree (BST)
- Left child < Parent < Right child
- Enables efficient searching

<br>
Binary Tree Traversals<br>
1. Inorder (Left → Root → Right)
- Result for example above: 3, 5, 7, 10, 15, 20, 25<br>

2. Preorder (Root → Left → Right)
- Result: 10, 5, 3, 7, 20, 15, 25<br>

3. Postorder (Left → Right → Root)
- Result: 3, 7, 5, 15, 25, 20, 10<br>

4. Level Order (BFS – level by level)
- Result: 10, 5, 20, 3, 7, 15, 25<br>

## Code Example (Python)
pythonclass Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

## class BinaryTree:
    def __init__(self):
        self.root = None

    def inorder(self, node):
        if node:
            self.inorder(node.left)
            print(node.data, end=" ")
            self.inorder(node.right)

    def preorder(self, node):
        if node:
            print(node.data, end=" ")
            self.preorder(node.left)
            self.preorder(node.right)

    def postorder(self, node):
        if node:
            self.postorder(node.left)
            self.postorder(node.right)
            print(node.data, end=" ")

## Usage
tree = BinaryTree()
tree.root = Node(10)
tree.root.left = Node(5)
tree.root.right = Node(20)
tree.root.left.left = Node(3)
tree.root.left.right = Node(7)

print("Inorder:  ", end=""); tree.inorder(tree.root)   # 3 5 7 10 20
print("\nPreorder: ", end=""); tree.preorder(tree.root) # 10 5 3 7 20
print("\nPostorder:", end=""); tree.postorder(tree.root)# 3 7 5 20 10

## Properties & Formulas
PropertyValueMax nodes at level l2^lMax nodes in tree of height h2^(h+1) - 1Min height for n nodes⌊log₂(n)⌋Max height for n nodesn - 1 (skewed)

## Time Complexity
OperationAverage (BST)Worst (Skewed)SearchO(log n)O(n)InsertO(log n)O(n)DeleteO(log n)O(n)TraversalO(n)O(n)

## Applications
- File systems – directory structure
- Databases – indexing (B-Trees)
- Compilers – expression/syntax trees
- AI – decision trees
- Networking – routing algorithms
- Heaps – priority queues
- Huffman Encoding – data compression

