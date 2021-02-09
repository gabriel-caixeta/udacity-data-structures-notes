# udacity-data-structures-notes

## 1. Introduction

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
- in the examples, word_flipper: `word = word[::-1]`　***FIND OUT WHAT IT DOES***

### Linked Lists
- Easier than arrays to add and remove elements (takes constant time)
- Stores the next element of the linked list
- Doubly Linked List (contains both previous and next elements' reference)
- Nodes don't have to be next to each other in memory
***Only used in OOP ??***

#### Types of Linked Lists
1. Singly Linked Lists
    -  Contains a reference to the next element

2. Doubly Linked Lists
    - Contains a reference to both the next and previous element

3. Circular Linked Lists
    - Contains a reference to another node within itself (not necessarily the head one)
    - ie. NodeA -> NodeB -> NodeC -> NodeD -> NodeB

