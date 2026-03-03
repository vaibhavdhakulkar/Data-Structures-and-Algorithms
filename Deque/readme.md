# DEQUE (DOUBLE ENDED QUEUE)
## 1. Introduction
- In computer science, a queue is a linear data structure that follows the principle of FIFO (First In First Out).
- However, in a normal queue:
- Insertion is allowed only at the rear end
- Deletion is allowed only at the front end
- To overcome this limitation, a more flexible data structure called Deque (Double Ended Queue) was introduced.
- A deque allows insertion and deletion of elements at both ends of the structure.

## 2. Definition of Deque
- A Deque (Double Ended Queue) is a linear data structure in which:
- Insertion and deletion operations can be performed at both the front and the rear ends.
- It is called double ended because both ends of the queue are open for operations.

## 3. Characteristics of Deque
The main characteristics of a deque are:
- It is a linear data structure.
- It allows insertion at both ends (front and rear).
- It allows deletion at both ends (front and rear).
- It does not strictly follow FIFO like a normal queue.

### It can behave as both:
- Stack (LIFO)
- Queue (FIFO)
- It provides more flexibility than a normal queue.

## 4. Types of Deque
- Deque is divided into two main types:

### 4.1 Input Restricted Deque
In an Input Restricted Deque:
- Insertion is allowed only at one end (usually rear).
- Deletion is allowed at both ends (front and rear).

### Diagram:
- Insert → Rear only
- Delete → Front and Rear

### Example:
If insertion is allowed only at rear:
- InsertRear(10) → [10]
- InsertRear(20) → [10, 20]
- DeleteFront() → [20]
- DeleteRear() → [ ]

### 4.2 Output Restricted Deque
In an Output Restricted Deque:
- Deletion is allowed only at one end (usually front).
- Insertion is allowed at both ends (front and rear).

### Diagram:
- Insert → Front and Rear
- Delete → Front only

### Example:
- InsertRear(10) → [10]
- InsertFront(5) → [5, 10]
- DeleteFront() → [10]

## 5. Operations on Deque
The basic operations performed on a deque are:
- InsertFront(x) – Inserts element x at the front end.
- InsertRear(x) – Inserts element x at the rear end.
- DeleteFront() – Removes the element from the front end.
- DeleteRear() – Removes the element from the rear end.
- GetFront() – Returns the front element.
- GetRear() – Returns the rear element.
- isEmpty() – Checks whether the deque is empty.
- isFull() – Checks whether the deque is full.

## 6. Representation of Deque
Deque can be represented using:
- Array
- Linked List
- Circular Array

### 6.1 Deque Using Array
In array implementation:
- Two pointers are used: front and rear.
- Elements are stored in a fixed-size array.
- Circular array technique is usually used to avoid memory wastage.

### Example:
Index:  0  1  2  3  4<br>
Deque: [5,10,20,__,__]<br>
Front = 0<br>
Rear = 2<br>

### 6.2 Deque Using Linked List
In linked list implementation:
Each node contains:
- Data
- Pointer to next node
- Pointer to previous node (in doubly linked list)
- Insertion and deletion are easier at both ends.

## 7. Algorithms for Deque Operations
Insert at Front<br>
Steps:
- Check if deque is full.
- If front is at beginning, move front circularly.
- Insert the new element.
- Update front pointer.
- Insert at Rear

<br>
Steps:<br>
- Check if deque is full.
- Move rear pointer forward.
- Insert element.
- Update rear.
- Delete from Front

<br>
Steps:
- Check if deque is empty.
- Remove front element.
- Move front pointer forward.
- Delete from Rear

<br>
Steps:
- Check if deque is empty.
- Remove rear element.
- Move rear pointer backward.

## 8. Applications of Deque
Deque is used in many practical applications such as:
- Palindrome checking
- Sliding window problems
- Undo and redo operations
- Job scheduling
- CPU scheduling
- Browser history
- Expression evaluation
- Task management systems

## 9. Advantages of Deque
- Flexible insertion and deletion.
- Can act as stack and queue.
- Efficient for dynamic data processing.
- Useful in complex algorithms.

## 10. Disadvantages of Deque
- More complex than simple queue.
- Implementation is harder.
- Requires careful pointer management.
- Fixed size in array implementation.

## 11. Comparison with Stack and Queue
- Feature	Stack	Queue	Deque
- Insertion	One end (top)	Rear	Front & Rear
- Deletion	One end (top)	Front	Front & Rear
- Principle	LIFO	FIFO	Both
- Flexibility	Low	Medium	High

##  13. Time Complexity
All major operations:
- InsertFront
- InsertRear
- DeleteFront
- DeleteRear
- ⏱ Time Complexity: O(1)

## 14. Example (Detailed)
Let the deque be empty.
Operations:
- InsertRear(10) → [10]
- InsertRear(20) → [10, 20]
- InsertFront(5) → [5, 10, 20]
- DeleteRear() → [5, 10]
- DeleteFront() → [10]

-- Final Deque:
[10]

## 14. Important Exam Notes
- Deque stands for Double Ended Queue.
- Two types: Input restricted and Output restricted.
- Insert & delete at both ends.
- Used in scheduling and window problems.
- Operations are O(1).

## 15. Conclusion
- A Deque (Double Ended Queue) is a powerful and flexible linear data structure that extends the functionality of a normal queue.
- It allows insertion and deletion at both ends and is widely used in system programming, scheduling, and algorithm design.
- It combines features of both stack and queue and provides high efficiency in managing data from both ends.
