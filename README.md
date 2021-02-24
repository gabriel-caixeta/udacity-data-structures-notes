# udacity-data-structures-notes

## 1. Introduction
### How to Solve Problems
#### Problem
- Is defined by the relation between the input and output
- Rules:
    - Find the inputs
    - Find the outputs
    - Solve the problem
- Think of ways to structure a code, so you're able to do meaninful tests as you go

### Efficiency
- Also known as complexity
- An arrangement between space and time: there's a need to sacrifice one for the other
- Big O notation can be used for both time and space (more used in time)
- [Big O Algorithm Complexity Cheat Sheet](https://www.bigocheatsheet.com/)
- ***Need to work a bit more with Big O way of thinking***

## 2. Data Structures
### 1. Collection
- No particular order (can't get a specifc element,ie. the third element)
- Don't have to have objects of the same type

### 2. Lists (not in Python)
- Have an order (can get a specifc element)
- Have no fixed lenght (can add or remove elements)

### 3. Arrays and Python Lists
- Is a list with a few added rules
- Has an index (lists do not)
- Python lists are basically arrays with added high-level functionality
- The elements are next to each other in memory, therefore, with the index, you can easily access a specific element

### 4. Strings
- Arrays of bytes representing uUnicode characters

- Question: in the examples, word_flipper: `word = word[::-1]`　***FIND OUT WHAT IT DOES***

### 5. Linked Lists
- Easier than arrays to add and remove elements (takes constant time)
- Stores the next element of the linked list
- Doubly Linked List (contains both previous and next elements' reference)
- Nodes don't have to be next to each other in memory

- **Question**: Only used in OOP ?
    - Answer: No. Will alocate a few bytes for next element location, and other bytes for the actual value.

#### 5.1 Types of Linked Lists
1. Singly Linked Lists
    -  Contains a reference to the next element

2. Doubly Linked Lists
    - Contains a reference to both the next and previous element

3. Circular Linked Lists
    - Contains a reference to another node within itself (not necessarily the head one)
    - ie. NodeA -> NodeB -> NodeC -> NodeD -> NodeB

### 6. Stacks
- Useful when the most recent elements / order of which the elements were saved is more important
- Can be implemented with different Data Types (Array, Linked List, etc)
- Can only access things from one end

#### 6.1 Terminology
- push: add an element to the stack (not insert)
- pop: take an element off of the stack (not remove)
- LIFO (Last In, First Out): the last element you push in, is the first one you get when you use pop

### 7. Queues
- Opposite of a stack -> FIFO (First In, First Out)
- Can be implemented with a LinkedList

### 7.1 Terminology
- First/Oldest element : head
- Last/ Newest element: Tail
- Add to end of queue: Enqueue
- Remove first element: Dequeue
- Look at head element but don't remove: peek

### 7.2 Types of Queues
- Deque ("Deck"):
    - Double ended queue (queue that goes both ways)
    - Can Enqueue or Dequeue from either end
- Priority Queue:
    - Assign each element with a numerical priority
    - When Dequeue, remove the element with the highest priority
    - When with the same priority, oldest element gets dequeued first

### 8. Recursion
- What it needs:
    - Base case: an exit condition, used to avoid infinite recursion
    - Call itself with a different input parameter, also to avoid infinite recursion
- Things to watch out for:
    - Call Stack: python has a limit on the depth of recursion to prevent a stack overflow
    - Slicing: (`a[start:end]`) is of O(k), where k is numbers of items to be sliced, so if it is included in the recursion, might increase the time complexity
- Practice:
    - Factorial
    - Reverse a string
    - Palindrome check ("abba", "madam")
    - Add one to list representing a number (ie. [1,2,3])
    - List permutation - uses insert to add to list -> needs deep copy
    - String permutation - can't insert on string, no need for deep copy
    - Keypad combinations
    - Deep reverse: reverse nested lists (ie. `[1,2,3,[4,5,6]]` becomes `[[6,5,4],3,2,1]`)
    - Tower of Hanoi - ***MIND BLOWING***

### 8.1 Call Stack
- Is a stack (LIFO) of frames
- Frames
    - when we call a function a frame is created in memory
    - all the variables local to the function are created in this memory frame
    - as soon as it is created it is pushed onto the call stack
- The frame on top of the stack is executed first, as soon as the function finishes executing, the frame is discarted from the **call stack**
- Tool for visualization: (Python tutor)[http://pythontutor.com/]
-  