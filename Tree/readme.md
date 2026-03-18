# 📁 Tree Data Structure (Basic → Advanced)
## 🌳 What is a Tree?
A Tree is a non-linear hierarchical data structure consisting of nodes connected by edges.
- The top node is called the Root
- Each node can have children
- Nodes without children are called Leaf nodes<br>
👉 Unlike arrays/linked lists (linear), trees represent hierarchical relationships

## 🧱 Basic Terminology
- Term:	Meaning
- Root:	Topmost node
- Parent:	Node having children
- Child:	Node derived from parent
- Leaf:	Node with no children
- Height:	Longest path from root to leaf
- Depth:	Distance from root to a node
- Subtree:	Tree formed by a node and its descendants

## 🌲 Types of Trees:
### 1. Binary Tree
Each node has at most 2 children:
- Left child
- Right child
        10
       /  \
      5    20
      
### 2. Binary Search Tree (BST)
A special binary tree where:<br>
👉 Left < Root < Right
        10
       /  \
      5    20
      
✔️ Left subtree contains smaller values
✔️ Right subtree contains greater values

## 🔁 Tree Traversal (VERY IMPORTANT 🔥)
Traversal = Visiting all nodes in a tree

### 1. Inorder Traversal (Left → Root → Right)
👉 For BST → gives sorted output
def inorder(root):
    if root:
        inorder(root.left)
        print(root.val)
        inorder(root.right)
        
### 2. Preorder Traversal (Root → Left → Right)
👉 Used to copy/clone tree
def preorder(root):
    if root:
        print(root.val)
        preorder(root.left)
        preorder(root.right)
        
### 3. Postorder Traversal (Left → Right → Root)
👉 Used for deleting tree
def postorder(root):
    if root:
        postorder(root.left)
        postorder(root.right)
        print(root.val)
        
## 📏 Height of a Tree:
Height = Longest path from root to leaf
def height(root):
    if root is None:
        return -1   # or 0 depending on definition
    return 1 + max(height(root.left), height(root.right))
    
## ⚙️ Binary Search Tree Operations
### 🔍 Search in BST
def search(root, key):
    if root is None or root.val == key:
        return root
    if key < root.val:
        return search(root.left, key)
    return search(root.right, key)
    
### ➕ Insert in BST
def insert(root, key):
    if root is None:
        return Node(key)
    if key < root.val:
        root.left = insert(root.left, key)
    else:
        root.right = insert(root.right, key)
    return root
    
### ❌ Delete in BST (Important Case Handling)
Cases:
- Node is leaf → remove directly
- Node has one child → replace with child
- Node has two children → replace with inorder successor

## ⚡ Time Complexity
- Operation	Time Complexity
- Search	O(log n) (balanced)
- Insert	O(log n)
- Delete	O(log n)
- Worst Case	O(n) (skewed tree)

## 🌐 Real-World Applications
- File systems (folders structure)
- Database indexing
- Searching algorithms
- Hierarchical data (org structure)

## 🚀 Advanced Concepts
- Once basics are clear, move to:
- AVL Trees (Self-balancing BST)
- Red-Black Trees
- Heaps (Priority Queue)

Trie (String searching)

Segment Trees
