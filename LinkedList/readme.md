# Linked List
A Linked List is a linear data structure in which elements are stored in separate memory locations and connected using pointers (or references).

Unlike arrays, linked lists do not store elements in contiguous memory locations. Instead, each element (called a node) contains:
- Data – the actual value
- Pointer / Reference – the address of the next node in the list<br>
Because of this structure, linked lists allow efficient insertion and deletion operations without shifting elements like arrays.

## Structure of a Linked List Node
Each node typically contains two parts:
Node
 ├── Data
 └── Next Pointer

Example:
[10 | next] → [20 | next] → [30 | next] → NULL

Explanation:
First node stores 10
Second node stores 20
Third node stores 30
Last node points to NULL, indicating the end of the list
The starting point of the linked list is called the Head.

## Types of Linked Lists
1. Singly Linked List
Each node contains:
Data
Pointer to the next node

Example:
Head → [10] → [20] → [30] → NULL
Traversal is only in one direction.

2. Doubly Linked List
Each node contains:
Data
Pointer to the next node
Pointer to the previous node

Example:
NULL ← [10] ⇄ [20] ⇄ [30] → NULL
Traversal is possible both forward and backward.

3. Circular Linked List: In this structure, the last node points back to the first node instead of NULL.

Example:
[10] → [20] → [30]
  ↑             ↓
  └─────────────┘

This forms a loop.

4. Basic Operations in Linked Lists
1. Traversal: Traversal means visiting each node in the linked list.

Algorithm
- Start from the head
- Print or process the node data
- Move to the next node
- Repeat until NULL is reached

Example Code (Python)
def traverse(head):
    current = head
    while current:
        print(current.data)
        current = current.next

2. Insertion
Insertion can occur at different positions.

1. Insertion at Beginning
Steps:
Create a new node
Point new node’s next to current head
Move head to new node

Example:
Before:
10 → 20 → 30
Insert 5

After:
5 → 10 → 20 → 30

Python Example
def insert_at_beginning(head, data):
    new_node = Node(data)
    new_node.next = head
    head = new_node
    return head
    
## Insertion at End
Steps:
Traverse to last node
Create new node
Set last node next to new node

Example:
Before:
10 → 20 → 30
Insert 40

After:
10 → 20 → 30 → 40

## Insertion at Specific Position
Steps:
Traverse to desired position
Update pointers

Example:
Insert 25 after 20
10 → 20 → 25 → 30

## Deletion
Deletion removes a node from the linked list.

1. Delete First Node
Steps:
Move head to next node
Remove old head

Example:
Before
10 → 20 → 30

After deleting first node
20 → 30

## Python Example
def delete_first(head):
    if head is None:
        return None
    head = head.next
    return head

## Delete Last Node
Steps:
Traverse until second-last node
Set its next to NULL

Example:
Before
10 → 20 → 30

After
10 → 20

## Reversal of Linked List
Reversing means changing the direction of links.

Example:
Before
10 → 20 → 30 → NULL

After
30 → 20 → 10 → NULL
Python Implementation
def reverse(head):
    prev = None
    current = head

    while current:
        next_node = current.next
        current.next = prev
        prev = current
        current = next_node
    return prev
    
## Time Complexity
- Operation	Time Complexity
- Traversal	O(n)
- Insertion at beginning	O(1)
- Insertion at end	O(n)
- Deletion	O(n)
- Searching	O(n)

## Advantages of Linked List
- Dynamic size (can grow or shrink)
- Efficient insertion and deletion
- No memory wastage due to shifting elements
- Useful for implementing other data structures

## Disadvantages
- Extra memory required for pointers
- No direct access like arrays
- Traversal is slower compared to arrays

## Applications of Linked Lists
- Linked lists are used in:
- Implementation of Stacks
- Implementation of Queues
- Hash Tables
- Graph adjacency lists
- Memory management
- Undo functionality in software

## Example Implementation (Full)
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None


## class LinkedList:

    def __init__(self):
        self.head = None

    def insert(self, data):
        new_node = Node(data)

        if self.head is None:
            self.head = new_node
            return

        temp = self.head
        while temp.next:
            temp = temp.next

        temp.next = new_node

    def display(self):
        temp = self.head
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
