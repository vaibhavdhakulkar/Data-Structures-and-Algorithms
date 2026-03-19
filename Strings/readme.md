# 📁 Strings (Data Structure)
## 🔤 What is a String?
- A String is a sequence of characters enclosed within quotes ("" or '').
- It is one of the most commonly used data structures for handling text-based data.
- s = "Hello World"<br>
👉 Strings are immutable in Python (cannot be changed directly).<br>

## 🧱 Basic Concepts
Concept	Description
- Indexing:  Access characters using position (0-based)
- Slicing:  Extract substring using range
- Length:  Number of characters (len())
- Immutability:  Cannot modify directly

## 🔍 Common String Operations
### 1. Indexing
s = "Python"<br>
print(s[0])  # P<br>
print(s[-1]) # n<br>

### 2. Slicing
s = "Python"<br>
print(s[0:4])  # Pyth<br>
print(s[::-1]) # Reverse<br>

### 3. String Length
len("Hello")  # 5<br>

## 🔁 Important Problems (Interview Focus 🔥)
### 1. Reverse a String
def reverse_string(s):<br>
    return s[::-1]<br>

### 2. Palindrome Check
👉 A string that reads same forward and backward<br>
def is_palindrome(s):<br>
    return s == s[::-1]<br>

### 3. Count Characters
from collections import Counter<br>
def count_chars(s):<br>
    return Counter(s)<br>

### 4. Substring Check
def is_substring(s, sub):<br>
    return sub in s<br>

### 5. Remove Duplicates
def remove_duplicates(s):<br>
    return "".join(set(s))<br>

### 6. Find First Non-Repeating Character
from collections import Counter<br>
def first_unique(s):<br>
    count = Counter(s)<br>
    for char in s:<br>
        if count[char] == 1:<br>
            return char<br>

🔎 Pattern Matching (Basic Idea)
👉 Used to find patterns in text
- Simple: in operator
- Advanced: Regular Expressions (regex)<br>
import re<br>
re.search("cat", "concatenate")<br>

## ⚡ Time Complexity
- Operation	Complexity
- Access	O(1)
- Traversal	O(n)
- Slicing	O(n)
- Search	O(n)

## 🌐 Real-World Applications
- Text processing (search engines)
- Data cleaning
- Password validation
- DNA sequence analysis
- Chat applications

## 🚀 Advanced Topics
- KMP Algorithm (pattern matching)
- Rabin-Karp Algorithm
- Trie (prefix matching)
- String hashing

## 🎯 Interview Focus
### 🔥 Must practice:
- Reverse string
- Palindrome
- Anagrams
- Substrings
- Frequency count
- Sliding window problems

### 🧠 Quick Tricks
- Reverse → [::-1]
- Palindrome → s == s[::-1]
- Count → Counter()
- Substring → in
