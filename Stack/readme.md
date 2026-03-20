# 📁 Stack (Data Structure)
A Stack is a linear data structure that works on the principle of Last In, First Out (LIFO). This means the element that is added last will be the first one to be removed. You can imagine it like a stack of plates — you place a new plate on top, and when you remove one, you always take the top plate first.<br>

In a stack, all operations such as insertion and deletion happen only at one end, called the top of the stack. This restriction makes stack operations very efficient and simple to manage. The main operations are push (to add an element), pop (to remove the top element), and peek (to view the top element without removing it).<br>

Stacks are widely used in programming because they help manage function calls, memory, and problem-solving patterns. For example, when a function is called, it is added to the call stack, and once it finishes execution, it is removed. This is how recursion works internally.<br>

Another important use of stacks is in solving problems like balanced parentheses, expression evaluation (postfix/prefix), and reversing data. Whenever a problem involves tracking previous elements or working in reverse order, stack becomes a very useful tool.<br>

## 💡 Simple Understanding
Think of stack like this:<br>
- You add (push) items only on top
- You remove (pop) items only from top
- You cannot access middle elements directly<br>
👉 That’s why it is called controlled access structure

## 🎯 Key Idea to Remember
Stack always follows LIFO (Last In, First Out) and operates only from one side (top), making it simple but very powerful in solving many real-world and coding problems.

### 👉 The last element added is the first one to be removed.
Example:<br>
Push → [1, 2, 3]<br>
Pop  → removes 3 first<br>

## 🧱 Basic Operations
Operation	Description
- Push:	Add element to top
- Pop:	Remove element from top
- Peek / Top:	View top element
- isEmpty:	Check if stack is empty

## 🛠️ Stack Implementation (Python)
Using List (Built-in)<br>
stack = []<br>

### #Push
stack.append(10)<br>
stack.append(20)<br>

### #Pop
stack.pop()

### #Peek
top = stack[-1]

### #Check empty
is_empty = len(stack) == 0<br>
Using Class (Custom Implementation)<br>
class Stack:<br>
    def __init__(self):<br>
        self.stack = []<br>

    def push(self, x):<br>
        self.stack.append(x)<br>

    def pop(self):<br>
        if not self.is_empty():<br>
            return self.stack.pop()<br>

    def peek(self):<br>
        return self.stack[-1] if not self.is_empty() else None<br>

    def is_empty(self):<br>
        return len(self.stack) == 0<br>
        
## 🔁 Important Problems (Interview Focus 🔥)
### 1. Balanced Parentheses
👉 Check if brackets are properly matched<br>
def is_valid(s):<br>
    stack = []<br>
    mapping = {')': '(', '}': '{', ']': '['}<br>

    for char in s:<br>
        if char in mapping:<br>
            top = stack.pop() if stack else '#'<br>
            if mapping[char] != top:<br>
                return False<br>
        else:<br>
            stack.append(char)<br>

    return not stack<br>
    
### 2. Reverse a String using Stack
def reverse_string(s):<br>
    stack = list(s)<br>
    result = ""<br>

    while stack:<br>
        result += stack.pop()<br>
    return result<br>
   
### 3. Evaluate Postfix Expression
def evaluate_postfix(expr):<br>
    stack = []<br>

    for char in expr<br>
        if char.isdigit():<br>
            stack.append(int(char))<br>
        else:<br>
            b = stack.pop()<br>
            a = stack.pop()<br>

            if char == '+': stack.append(a + b)<br>
            elif char == '-': stack.append(a - b)<br>
            elif char == '*': stack.append(a * b)<br>
            elif char == '/': stack.append(a // b)<br>
    return stack[0]<br>
    
### 4. Next Greater Element
def next_greater(arr):<br>
    stack = []<br>
    result = [-1] * len(arr)<br>

    for i in range(len(arr)):<br>
        while stack and arr[i] > arr[stack[-1]]:<br>
            index = stack.pop()<br>
            result[index] = arr[i]<br>
        stack.append(i)<br>
    return result<br>

## ⚡ Time Complexity
Operation	Complexity
- Push:	  O(1)
- Pop:	  O(1)
- Peek:	  O(1)

## 🌐 Real-World Applications
- Undo/Redo operations
- Expression evaluation (compilers)
- Browser history navigation
- Backtracking algorithms
- Function call stack (recursion)

## 🚀 Advanced Concepts
- Monotonic Stack
- Stack using Queue
- Min Stack (get min in O(1))
- Expression Conversion (Infix → Postfix/Prefix)

## 🎯 Interview Focus
🔥 Must practice:<br>
- Balanced parentheses
- Next greater element
- Expression evaluation
- Min stack

## 🧠 Quick Tricks
- LIFO → Last In First Out
- Use stack for:
  - Matching problems
  - Reversal
  - “Nearest greater/smaller” problems
