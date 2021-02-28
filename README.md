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
    - Return codes - possible char for ASCII code (ie. 123 = [abc, aw, lc])
    - Return subsets of list
    - Staircase - how many ways to climb n steps if you can climb 1, 2 or 3 steps at a time
    - Last occurence of a element in an array

### 8.1 Call Stack
- Is a stack (LIFO) of frames
- Frames
    - when we call a function a frame is created in memory
    - all the variables local to the function are created in this memory frame
    - as soon as it is created it is pushed onto the call stack
- The frame on top of the stack is executed first, as soon as the function finishes executing, the frame is discarted from the **call stack**
- Tool for visualization: (Python tutor)[http://pythontutor.com/]

### 9. Trees
- Extension of a Linked List
- Characteristics:
    - Must be completely connected: starting from the root, there must be some way to reach every element of the tree
    - There must not be any cycles

### 9.1 Terminology
- Root: first element (level 1)
- Nodes: elements of the tree
- Level: indicates the distance from the root (root is level 1, first nodes are level 2, etc)
- Parent/Child: node at a lower level is a parent, connected to a node at a higher level, that is a child
    - Nodes in the middle can be both Parent and Child. Depends on what it is being compared it to
    - Children can only have one parent
- Ancestry: node at a lower level (Ancestor), connected to a node at a higher level (Descendant)
- Leaves/External nodes: nodes at the end, that have no child nodes
- Height: is the distance between a node and the furthest connected leaf
    - Leaves have height 0
    - Height of a tree is the height of the root node
- Depth: opposite to the height

### 9.2 Tree Traversal
- Depth-First Search (DFS)
    - If there are children node to explore, they are a priority
    - Pre-order:
        - Check a node before moving on to the child nodes
    - In-order:
        - Left to right. Check all nodes to the left and traverse back (??)
    - Post-order:
        - Check off a node only after visiting all its children
- Breadth-First Search (BFS)
    - The priority is visiting every node on the same level we're currently on, before visiting child nodes
    - Level order
    - Usually visit nodes on the same level from left to right

### 9.2.1 Tree Traversal Recursion (DFS)
- Base code:
    - 1: visited.append(node.value)
    - 2: traverse(node.left)
    - 3: traverse(node.right)
- Pre-order: 1-2-3
- In-order: 2-1-3
- Post-order: 2-3-1
    



### 9.3 Binary Tree
- Parents have **at most two children**
- Search and delete(search the element before deleting) -> O(n)
- Insert: worst case is the height if the tree -> 0(logn)

### 9.3.1 Binary Search Tree (BST)
- All elements to the left of an element have lower value, to the right have higher value
- Search: order is the height of the tree ->  O(logn)
- Unbalanced BST: the distribution of nodes is skewed to one side
    - can start at the root, or any other node
    - is the worst case scenarion for a BST
    - search, insert, delete all take linear time -> O(n)