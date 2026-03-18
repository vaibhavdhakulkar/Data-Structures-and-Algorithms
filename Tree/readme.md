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
Each node has at most 2 children:<br>
- Left child
- Right child<br>
        10 <br>
       /  \ <br>
      5    20 <br>
      
### 2. Binary Search Tree (BST)
A special binary tree where:
- Left < Root < Right<br>
        10 <br>
       /  \ <br>
      5    20 <br>
✔️ Left subtree contains smaller values<br>
✔️ Right subtree contains greater values<br>

## 🔁 Tree Traversal (VERY IMPORTANT 🔥)
Traversal = Visiting all nodes in a tree

### 1. Inorder Traversal (Left → Root → Right)
👉 For BST → gives sorted output<br>
def inorder(root):<br>
    if root:<br>
        inorder(root.left)<br>
        print(root.val)<br>
        inorder(root.right)<br>
        
### 2. Preorder Traversal (Root → Left → Right)
👉 Used to copy/clone tree<br>
def preorder(root):<br>
    if root:<br>
        print(root.val)<br>
        preorder(root.left)<br>
        preorder(root.right)<br>
        
### 3. Postorder Traversal (Left → Right → Root)
👉 Used for deleting tree<br>
def postorder(root):<br>
    if root:<br>
        postorder(root.left)<br>
        postorder(root.right)<br>
        print(root.val)<br>
        
## 📏 Height of a Tree:
Height = Longest path from root to leaf<br>
def height(root):<br>
    if root is None:<br>
        return -1   # or 0 depending on definition<br>
    return 1 + max(height(root.left), height(root.right))<br>
    
## ⚙️ Binary Search Tree Operations
### 🔍 Search in BST
def search(root, key):<br>
    if root is None or root.val == key:<br>
        return root<br>
    if key < root.val:<br>
        return search(root.left, key)<br>
    return search(root.right, key)<br>
    
### ➕ Insert in BST
def insert(root, key):<br>
    if root is None:<br>
        return Node(key)<br>
    if key < root.val:<br>
        root.left = insert(root.left, key)<br>
    else:<br>
        root.right = insert(root.right, key)<br>
    return root<br>
    
### ❌ Delete in BST (Important Case Handling)
Cases:<br>
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
- Trie (String searching)
- Segment Trees
