# 📘 Array in Data Structure:
An array is a linear data structure that stores multiple elements of the same data type in contiguous (continuous) memory locations. 
Each element in the array is accessed using an index number, which usually starts from 0. Arrays allow fast and direct access to elements and are commonly used to store and manage large collections of data efficiently.

## 🔹 2. Characteristics / Properties of Array
- Same Data Type - All elements stored in an array must be of the same data type (int, float, char, etc.).
- Fixed Size - The size of an array is decided when it is created and cannot be changed in static arrays.
- Index-Based Access - Each element has a unique index value to identify its position.

## Example:
Index:  0   1   2   3<br>
Value: 10  20  30  40<br>
✅ Contiguous Memory<br>

All elements are stored in consecutive memory locations, which allows fast access.<br>

## 🔹 3. Types of Arrays
### 1️⃣ One-Dimensional Array (1D):
Stores elements in a single row.<br>
Example:<br>
int arr[5] = {1,2,3,4,5};<br>

### 2️⃣ Two-Dimensional Array (2D)
Stores elements in rows and columns (table form).<br>
Example:<br>
int arr[2][3] = {{1,2,3},{4,5,6}};<br>

### 3️⃣ Multi-Dimensional Array
- Arrays with more than two dimensions (3D, 4D, etc.).<br>

🔹 4. Operations on Array
🔸 Traversal - Accessing each element one by one.<br>
🔸 Insertion - Adding a new element at a specific position by shifting other elements.<br>
🔸 Deletion - Removing an element and shifting remaining elements.<br>
🔸 Searching - Finding an element using:<br>
- Linear Search
- Binary Search (sorted array)<br>
🔸 Updating - Changing the value at a given index.<br>
🔸 Sorting - Arranging elements in ascending or descending order.<br>

## 🔹 5. Time Complexity (Basic)
Operation	Time Complexity<br>
- Access	O(1)
- Search	O(n)
- Insert	O(n)
- Delete	O(n)

## 🔹 6. Advantages of Array:
✔ Fast access using index<br>
✔ Easy to use and understand<br>
✔ Efficient memory usage<br>
✔ Good for storing fixed-size data<br>
✔ Supports many algorithms (sorting, searching)<br>

## 🔹 7. Disadvantages of Array:
❌ Fixed size (cannot grow easily)<br>
❌ Insertion and deletion are slow<br>
❌ Memory wastage possible<br>
❌ Only same type of data allowed<br>
❌ Not flexible<br>

## 🔹 8. Applications of Array
- Store marks of students
- Store employee salary list
- Matrix operations
- Image processing (pixels)
- Sorting and searching algorithms
- Stack and Queue implementation
- Database indexing
- Scientific calculations

## 🔹 9. Real-Life Example
Think of an array as a row of numbered houses 🏠🏠🏠🏠
Each house has an address (index), and you can directly go to house number 3 without visiting others.

🔹 11. Array vs Linked List (Brief)
Array	Linked List
Fixed size	Dynamic size
Fast access	Slow access
Continuous memory	Random memory
Hard insert/delete	Easy insert/delete
