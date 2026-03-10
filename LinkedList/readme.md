# Linked List
A Linked List is a linear data structure in which elements are stored in separate memory locations and connected using pointers (or references).<br>

Unlike arrays, linked lists do not store elements in contiguous memory locations. Instead, each element (called a node) contains:
- Data – the actual value
- Pointer / Reference – the address of the next node in the list<br>
Because of this structure, linked lists allow efficient insertion and deletion operations without shifting elements like arrays.

## Structure of a Linked List Node
Each node typically contains two parts:<br>
Node<br>
 ├── Data<br>
 └── Next Pointer<br>
<br>
Example:<br>
[10 | next] → [20 | next] → [30 | next] → NULL<br>

Explanation:<br>
First node stores 10<br>
Second node stores 20<br>
Third node stores 30<br>
Last node points to NULL, indicating the end of the list<br>
The starting point of the linked list is called the Head.<br>

## Types of Linked Lists
### 1. Singly Linked List<br>
Each node contains:<br>
Data<br>
Pointer to the next node<br>

Example:<br>
Head → [10] → [20] → [30] → NULL<br>
Traversal is only in one direction.<br>

### 2. Doubly Linked List
Each node contains:<br>
Data<br>
Pointer to the next node<br>
Pointer to the previous node<br>

Example:<br>
NULL ← [10] ⇄ [20] ⇄ [30] → NULL<br>
Traversal is possible both forward and backward.<br>

### 3. Circular Linked List: In this structure, the last node points back to the first node instead of NULL.<br>
Example:<br>
[10] → [20] → [30]<br>
  ↑             ↓<br>
  └─────────────┘<br>
This forms a loop.<br>

### 4. Basic Operations in Linked Lists<br>
### 1. Traversal: Traversal means visiting each node in the linked list.<br>

Algorithm<br>
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

### 2. Insertion
Insertion can occur at different positions.

#### 1. Insertion at Beginning
Steps:<br>
Create a new node<br>
Point new node’s next to current head<br>
Move head to new node<br>

Example:
Before:<br>
10 → 20 → 30<br>
Insert 5<br>

After:<br>
5 → 10 → 20 → 30<br>

Python Example
def insert_at_beginning(head, data):
    new_node = Node(data)
    new_node.next = head
    head = new_node
    return head
    
#### 2. Insertion at End
Steps:<br>
Traverse to last node<br>
Create new node<br>
Set last node next to new node<br>

Example:<br>
Before:<br>
10 → 20 → 30<br>
Insert 40<br>

After:<br>
10 → 20 → 30 → 40<br>

#### 3. Insertion at Specific Position
Steps:<br>
Traverse to desired position<br>
Update pointers<br>

Example:
Insert 25 after 20<br>
10 → 20 → 25 → 30<br>

## Deletion
Deletion removes a node from the linked list.

#### 1. Delete First Node
Steps:<br>
Move head to next node<br>
Remove old head<br>

Example:<br>
Before<br>
10 → 20 → 30<br>

After deleting first node<br>
20 → 30<br>

## Python Example
def delete_first(head):
    if head is None:
        return None
    head = head.next
    return head

#### 2. Delete Last Node
Steps:<br>
Traverse until second-last node<br>
Set its next to NULL<br>

Example:<br>
Before<br>
10 → 20 → 30<br>

After<br>
10 → 20<br>

## Reversal of Linked List
Reversing means changing the direction of links.

Example:<br>
Before<br>
10 → 20 → 30 → NULL<br>

After<br>
30 → 20 → 10 → NULL<br>
Python Implementation<br>
def reverse(head):<br>
    prev = None<br>
    current = head<br>

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
class Node:<br>
    def __init__(self, data):<br>
        self.data = data<br>
        self.next = None<br>


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
