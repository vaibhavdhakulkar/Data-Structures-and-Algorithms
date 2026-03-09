# Hashing
- Hashing is a technique used in computer science to store and retrieve data quickly using a special data structure called a hash table.
- It works by converting a key (input data) into a unique index using a function called a hash function.
- This index is then used to store or access the value directly, which makes operations like searching, inserting, and deleting very fast, usually in O(1) time complexity.
- In simple words: Hashing is a method of mapping data to a fixed index using a hash function for fast data access.

## Key Components of Hashing
### 1️⃣ Hash Function: A hash function takes input data (key) and converts it into a numeric index.
Example:<br>
hash(key) = index

Example:<br>
hash("apple") → 3<br>
hash("banana") → 7<br>
This index tells the computer where to store the value in memory.<br>

### 2️⃣ Hash Table: A hash table is a data structure that stores key–value pairs.
Example structure:<br>
Index	Key	Value<br>
0	–	–<br>
1	age	25<br>
2	name	Vaibhav<br>
3	city	Pune<br>

### 3️⃣ Key–Value Pair
Data is stored in the form:<br>
Key → Value<br>

Example:
"name" → "Vaibhav"<br>
"age" → 25<br>
"city" → "Pune"<br>

## Why Hashing is Used
Hashing is used to improve performance in programs where frequent searching or lookup operations are required.

### Advantages:
- Very fast data lookup
- Efficient memory access
- Used in many real-world systems

### Time Complexity
Operation	Time Complexity
- Insert	O(1)
- Search	O(1)
- Delete	O(1)

## Example of Hashing
Suppose we want to count the frequency of numbers in a list.

List:<br>
[1,2,2,3,4,4,4]<br>

Using hashing we store frequency:
Number	Frequency<br>
1	1<br>
2	2<br>
3	1<br>
4	3<br>

Hash table representation:
{<br>
1:1,<br>
2:2,<br>
3:1,<br>
4:3<br>
}<br>

## Hashing in Python
In Python, hashing is implemented using Dictionary (dict) and Set.

Example 1: Hash Map (Dictionary)<br>
Syntax<br>
hash_map = {}<br>

Example:<br>
numbers = [1,2,2,3,4,4,4]<br>

freq = {}<br>

for num in numbers:<br>
    if num in freq:<br>
        freq[num] += 1<br>
    else:<br>
        freq[num] = 1<br>
print(freq)<br>

Output: <br>
{1:1, 2:2, 3:1, 4:3}

Explanation:<br>
Dictionary stores numbers as keys<br>
Frequency as values<br>
Lookup happens very fast.<br>

## Hash Set Example:
A Hash Set stores unique elements only.

Syntax:<br>
my_set = set()<br>

Example:<br>
nums = [1,2,2,3,4,4]<br>
unique = set(nums)<br>
print(unique)<br>

Output:<br>
{1,2,3,4}

Explanation:<br>
Set automatically removes duplicate elements.

## Real Life Examples of Hashing
Hashing is widely used in:<br>
1️⃣ Databases: Fast data retrieval.<br>
2️⃣ Password Storage: Passwords are stored using hash functions for security.<br>
3️⃣ Caching Systems: Used in applications like web browsers.<br>
4️⃣ Data Deduplication: Finding duplicate files.<br>

## Common Problems Using Hashing
Examples of interview questions:
- Two Sum problem
- Find duplicates in array
- Group Anagrams
- Longest consecutive sequence
- Subarray sum equals K
- First non-repeating character

## Simple Visualization
Example list:<br>
["apple","banana","mango"]<br>

Hash function converts to index:
hash("apple") → 2<br>
hash("banana") → 5<br>
hash("mango") → 7<br>

Stored in hash table:
index 2 → apple<br>
index 5 → banana<br>
index 7 → mango<br>

## Summary
- Concept	Meaning
- Hashing	Mapping data to index
- Hash Function	Converts key → index
- Hash Table	Stores key–value pairs
- Hash Map	Dictionary in Python
- Hash Set	Stores unique values
