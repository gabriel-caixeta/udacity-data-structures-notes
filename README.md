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
### Collection
- No particular order (can't get a specifc element,ie. the third element)
- Don't have to have objects of the same type

### Lists (not in Python)
- Have an order (can get a specifc element)
- Have no fixed lenght (can add or remove elements)

### Arrays and Python Lists
- Is a list with a few added rules
- Has an index (lists do not)
- Python lists are basically arrays with added high-level functionality
- The elements are next to each other in memory, therefore, with the index, you can easily access a specific element

### Strings
- Arrays of bytes representing uUnicode characters

- Question: in the examples, word_flipper: `word = word[::-1]`　***FIND OUT WHAT IT DOES***

### Linked Lists
- Easier than arrays to add and remove elements (takes constant time)
- Stores the next element of the linked list
- Doubly Linked List (contains both previous and next elements' reference)
- Nodes don't have to be next to each other in memory

- Question: Only used in OOP ?
- Answer: No. Will alocate a few bytes for next element location, and other bytes for the actual value.

#### Types of Linked Lists
1. Singly Linked Lists
    -  Contains a reference to the next element

2. Doubly Linked Lists
    - Contains a reference to both the next and previous element

3. Circular Linked Lists
    - Contains a reference to another node within itself (not necessarily the head one)
    - ie. NodeA -> NodeB -> NodeC -> NodeD -> NodeB

