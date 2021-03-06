# Udacity - Data Structure and Algorithms - Personal Notes

# Table of Contents
- [Udacity - Data Structure and Algorithms - Personal Notes](#udacity---data-structure-and-algorithms---personal-notes)
- [Table of Contents](#table-of-contents)
- [1. Introduction](#1-introduction)
  - [How to Solve Problems](#how-to-solve-problems)
    - [Problem](#problem)
  - [Efficiency](#efficiency)
- [2. Data Structures](#2-data-structures)
  - [1. Collection](#1-collection)
  - [2. Lists (not in Python)](#2-lists-not-in-python)
  - [3. Arrays and Python Lists](#3-arrays-and-python-lists)
  - [4. Strings](#4-strings)
  - [5. Linked Lists](#5-linked-lists)
    - [5.1 Types of Linked Lists](#51-types-of-linked-lists)
  - [6. Stacks](#6-stacks)
    - [6.1 Terminology](#61-terminology)
  - [7. Queues](#7-queues)
    - [7.1 Terminology](#71-terminology)
    - [7.2 Types of Queues](#72-types-of-queues)
  - [8. Recursion](#8-recursion)
    - [8.1 Call Stack](#81-call-stack)
  - [9. Trees](#9-trees)
    - [9.1 Terminology](#91-terminology)
    - [9.2 Tree Traversal](#92-tree-traversal)
      - [9.2.1 Tree Traversal - DFS](#921-tree-traversal---dfs)
      - [9.2.2 Tree Traversal - BFS](#922-tree-traversal---bfs)
    - [9.3 Binary Tree](#93-binary-tree)
      - [9.3.1 Binary Search Tree (BST)](#931-binary-search-tree-bst)
  - [10. Set](#10-set)
  - [11. Hash Maps](#11-hash-maps)
    - [11.1 Maps](#111-maps)
    - [11.2 Hash Functions](#112-hash-functions)
- [3. Algorithms](#3-algorithms)
  - [1 Binary Search](#1-binary-search)
  - [2 Trie](#2-trie)
  - [3 Heap](#3-heap)
    - [3.1 Heapify](#31-heapify)
  - [4 Self Balancing Tree (Red - Black Tree)](#4-self-balancing-tree-red---black-tree)
    - [4.1 Insertion](#41-insertion)
  - [5 Sorting](#5-sorting)
    - [5.1 Bubble Sort](#51-bubble-sort)
      - [Time complexity](#time-complexity)
      - [Space complexity](#space-complexity)
      - [Algorithm](#algorithm)
    - [5.2 Merge Sort](#52-merge-sort)
      - [Time complexity](#time-complexity-1)
      - [Space complexity](#space-complexity-1)
      - [Algorithm](#algorithm-1)
    - [5.3 Quick Sort](#53-quick-sort)
      - [Time complexity](#time-complexity-2)
      - [Space complexity](#space-complexity-2)
      - [Algorithm](#algorithm-2)
    - [5.4 HeapSort](#54-heapsort)
      - [Algorithm](#algorithm-3)
- [Advanced Algorithms](#advanced-algorithms)
  - [Greedy Algorithms](#greedy-algorithms)
    - [Definition](#definition)
    - [Examples](#examples)
  - [Graph](#graph)
    - [Search](#search)
      - [DFS (Depth-First Search)](#dfs-depth-first-search)
      - [BFS (Breadth-First Search)](#bfs-breadth-first-search)

# 1. Introduction
## How to Solve Problems
### Problem
- Is defined by the relation between the input and output
- Rules:
    - Find the inputs
    - Find the outputs
    - Solve the problem
- Think of ways to structure a code, so you're able to do meaninful tests as you go

## Efficiency
- Also known as complexity
- An arrangement between space and time: there's a need to sacrifice one for the other
- Big O notation can be used for both time and space (more used in time)
- [Big O Algorithm Complexity Cheat Sheet](https://www.bigocheatsheet.com/)
- ***Need to work a bit more with Big O way of thinking***

# 2. Data Structures
## 1. Collection
- No particular order (can't get a specifc element,ie. the third element)
- Don't have to have objects of the same type

## 2. Lists (not in Python)
- Have an order (can get a specifc element)
- Have no fixed lenght (can add or remove elements)

## 3. Arrays and Python Lists
- Is a list with a few added rules
- Has an index (lists do not)
- Python lists are basically arrays with added high-level functionality
- The elements are next to each other in memory, therefore, with the index, you can easily access a specific element

## 4. Strings
- Arrays of bytes representing uUnicode characters

- Question: in the examples, word_flipper: `word = word[::-1]`　***FIND OUT WHAT IT DOES***

## 5. Linked Lists
- Easier than arrays to add and remove elements (takes constant time)
- Stores the next element of the linked list
- Doubly Linked List (contains both previous and next elements' reference)
- Nodes don't have to be next to each other in memory

- **Question**: Only used in OOP ?
    - Answer: No. Will alocate a few bytes for next element location, and other bytes for the actual value.

### 5.1 Types of Linked Lists
- Singly Linked Lists
    -  Contains a reference to the next element

- Doubly Linked Lists
    - Contains a reference to both the next and previous element

- Circular Linked Lists
    - Contains a reference to another node within itself (not necessarily the head one)
    - ie. NodeA -> NodeB -> NodeC -> NodeD -> NodeB

## 6. Stacks
- Useful when the most recent elements / order of which the elements were saved is more important
- Can be implemented with different Data Types (Array, Linked List, etc)
- Can only access things from one end

### 6.1 Terminology
- push: add an element to the stack (not insert)
- pop: take an element off of the stack (not remove)
- LIFO (Last In, First Out): the last element you push in, is the first one you get when you use pop

## 7. Queues
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

## 8. Recursion
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
- Tool for visualization: [Python tutor](http://pythontutor.com/)

## 9. Trees
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

#### 9.2.1 Tree Traversal - DFS
- Stack
- Recursiom
    - Base code:
        - 1: visited.append(node.value)
        - 2: traverse(node.left)
        - 3: traverse(node.right)
    - Pre-order: 1-2-3
    - In-order: 2-1-3
    - Post-order: 2-3-1

#### 9.2.2 Tree Traversal - BFS
- Queue
    - Can be used to print the tree in a visually pleasing way (each level in a line)


### 9.3 Binary Tree
- Parents have **at most two children**
- Search and delete(search the element before deleting) -> O(n)
- Insert: worst case is the height if the tree -> 0(logn)

#### 9.3.1 Binary Search Tree (BST)
- All elements to the left of an element have lower value, to the right have higher value
- Search: order is the height of the tree ->  O(logn)
- Unbalanced BST: the distribution of nodes is skewed to one side
    - can start at the root, or any other node
    - is the worst case scenarion for a BST
    - search, insert, delete all take linear time -> O(n)

## 10. Set
- A kind of collection, similar to a list, but that doesn't allow element repetition
- There is no particular order

## 11. Hash Maps
### 11.1 Maps
- Defining characteristic is the key-value structure
- Is a set based data structure
    - the keys in a map are a set

### 11.2 Hash Functions
- A hash function is any function that can be used to map data of arbitrary size to fixed-size values. The values returned by a hash function are called hash values, hash codes, digests, or simply hashes. The values are usually used to index a fixed-size table called a hash table. Use of a hash function to index a hash table is called hashing or scatter storage addressing. - [Source](https://en.wikipedia.org/wiki/Hash_function)
- Collisions: happens when the hash function returns the same value for two different inputs
    - Store in a bucket. instead of storing a value, you store a collection of the values with the same hash code in the same bucket
- It often requires a compromise between a wide spread array (uses more space), or a shorter array with larger buckets (can end up in a linear time complexity in the worst case scenario)

# 3. Algorithms
- is a high-level description of a trick for solving a problem

## 1 Binary Search
- Logic:
    - Get middle element of a sorted collection
    - Compare desired element with the middle
    - if desired is bigger, repeat with the higher half
    - else, repeat with the lower half
- Time complexity: `O(logn)`
    - Results Table:

        | Array Size | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
        | ---------- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
        | Itterations | 0 | 1 | 2 | 2 | 3 | 3 | 3 | 3 | 4 |

## 2 Trie
- Is a Tree data structure
- Good for dealing with sequence data (characters, words, network of nodes)
- Example:
    ```
    'a': {
        'd': {
            'd': {'word_end': True},
            'word_end': False
        },
        'word_end': True
    },
    'h': {
        'i': {'word_end': True},
        'word_end': False
    }
    ```

## 3 Heap
- Is a Tree data structure
    - Is a complete Binary Tree
- Elements are arranged in an increasing or decreasing order, in such that the root element is either the maximum or the minimum element of the tree
- MaxHeap
    - Parent has a grater value than the children
- MinHeap
    - Parent has a lower value than the children

### 3.1 Heapify
- Operation to reorder the tree based on the Heap properties
- Used when inserting or deleting elements in a Heap
- Insertion:
    - Add the element to the next open spot in the tree (last layer)
    - Check the parent, and swap when the child is bigger(MaxHeap)
- Deletion
    - Get the right most element and add to the deleted element place
    - Swap with the children on the left side if the children is bigger(MaxHeap)

## 4 Self Balancing Tree (Red - Black Tree)
- Minimizes the number of level that it uses
- Rules:
  - Color property: Nodes are assigned an aditional color property (red or black)
  - Null leaf nodes: every node that has no children, must have null children
  - If a node is red, both the children must be black
  - Root node must be black (optional)
  - **Every path from a node to its descendants null nodes must contain the same number of black nodes**
### 4.1 Insertion
- Time complexity: O(logn) for both average and worst cases
- Rule: Insert a node as a red node
- Cases:
  - Case 1 - Root node
    - insert the node to black if that is a rule
  - Case 2 - new parent node is black
    - no work needed
  - Case 3 - new parent node and its sibling are red
    - both changed to black
    - grandparent changed to red
  - new parent node is red and its sibling is black
    - Case 4 - node and parent are opposite (node is left child, parent is right child)
      - left rotation
    - Case 5 - node and parent are same side (node and parent are left child of their respective parents)
      - right rotation including grandparent
      - swap parent and grandparent's colors

## 5 Sorting
- Naive approach: check every element agains every other element in the array
- Consider if the sorting algorithm is **inplace** or not
  - inplace: swap elements within the array and does not need to create a new sorted array

### 5.1 Bubble Sort
- is naive approach
- an inplace algorithm
#### Time complexity
- Worst case, Average case = `O(n^2)`
- Best case = `O(n)`
  - when the array was already sorted, or if there's only one element the needs to be bubbled up to a new place
#### Space complexity
- `O(1)`
#### Algorithm
- Double loops

### 5.2 Merge Sort
- Devide and Conquer
#### Time complexity
- O([# of comparisons] * [# steps])
  - Comparisons can be approximated to `n`
  - Steps are as follows:
  - 
        | Array Size | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
        | ---------- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
        | Itterations | 0 | 1 | 2 | 2 | 3 | 3 | 3 | 3 | 4 |

- Worst, average case = `O(nlogn)`
#### Space complexity
- There's need to create new arrays
- Auxiliary Space = `O(n)`
#### Algorithm
- Devide the array into arrays of 1 or 2 elements
- Merge the arrays 2 by 2
- Repeat until merging all

### 5.3 Quick Sort
- Most efficient in most cases
#### Time complexity
- Worst case - `O(n^2)`
  - same as bubble sort
  - happens when the pivots are already in place
- Average and best case = `O(nlogn)`
#### Space complexity
- `O(1)`
#### Algorithm
- pick a pivot
  - usually the last element, but can be optimized by picking the median between the last few elements
- compare with the first element with the pivot
  - if the pivot is smaller, move the first element to the pivot location
  - the pivot to the location before it
  - and the element in that position to the first

    | Iterations/Array positions | 0 | 1 | 2 | 3 | 4 | 5 | 6 | Comments |
    | :--------: | --- | --- | --- | --- | --- | --- | --- | --- |
    | 0 | 8 | 3 | 1 | 7 | 0 | 10 | ***2*** | Select a pivot,  Compare and shift with *8* |
    | 1 | 10 | 3 | 1 | 7 | 0 | ***2*** | 8 | Compare and shift with *10* |
    | 2 | 0 | 3 | 1 | 7 | ***2*** | 10 | 8 | Compare and shift with *3* |
    | 3 | 0 | 7 | 1 | ***2*** | 3 | 10 | 8 | Compare and shift with *7* |
    | 4 | 0 | 1 | ***2*** | 7 | 3 | 10 | 8 | Compare with *0* and *1*, already on the right spot |
    | 5 | 0 | ***1*** | *2* | 7 | 3 | 10 | 8 | Select pivot, compare with *0*, already on the right spot |
    | 6 | *0* | *1* | *2* | 7 | 3 | 10 | ***8*** | Select pivot, compare with *7*, *3* and *10* and shift |
    | 7 | *0* | *1* | *2* | 7 | 3 | ***8*** | 10 | Already on the right spot |
    | 7 | *0* | *1* | *2* | 7 | ***3*** | *8* | *10* | Select new pivot, compare and shift with *7* |
    | 7 | *0* | *1* | *2* | *3* | *7* | *8* | *10* | Sorted |


### 5.4 HeapSort
- an in-place sorting algorithm

#### Algorithm
- convert the array into a maxheap
- swap the top element with the last element in the array
- repeat with `arr[*len(arr)-1]` (all but the sorted elements)

# Advanced Algorithms

## Greedy Algorithms
### Definition
- A Greedy Technique is the one which picks up the "best" possible solution to a sub-problem available at the moment. Greedy algorithms is the collective name given to algorithms which make use of the Greedy Technique. The step by step process of these algorithms may be different. However, if any algorithm follows the Greedy Technique at each step, it can be called as a Greedy Algorithm.
### Examples
- Dijkstra's Shortest Path Algorithm
- A* search Algorithm
- Prim's algorithm for Minimal Spanning Tree
- Kruskal's algorithm for Minimal Spanning Tree
- Knapsack Problem
- Travelling Salesman Problem
  
## Graph
- Data structure used to show how different things are connected to one another
- Tree is a type of Graph
- Disconnected graph
  - has a vertex that can't be reached by the other vertices
- Connectivity
  - Minimum number of elements that needs to be removed for a graph to become disconnected
- Representation
  - Edge List
    - List of the edges (ie. `[A,B]`)
  - Adjacency List
    - List of connected elements, the index of the adjacency list is the reference to the vertex it represents
    - `[[1], [0,2,3], [1,3], [1,2]]`
  - Adjacency Matrix
    - Diagonal is always zero
    - A single edge shows up twice in the matrix
    - `[[0,1,0,0], [1,0,1,1], [0,1,0,1], [0,1,1,0]]`

### Search
#### DFS (Depth-First Search)
- Mark a node as seen, add it to the seen elements stack
- Pick an edge, follow it, mark it as seen and add it to the stack
- Repeat while there are unseen edges and nodes
- When hit a node that you've seen before, go back one node and try another edge
- If you run out of edges with new nodes, pop the element from the stack and go back to the one before it
- Run time is often written as `O(|E| + |V|)` number of edges + vertices

#### BFS (Breadth-First Search)
- Similar to DFS, but here, we search every edge of one node before continuing to the next node
- Mark node as seen
- Then visit a node adjacent to it, mark it as seen and add it to a queue
- Go back to that first node and visit all the other adjacent, marking each as seen and adding to the queue
- When run out of edges, dequeue a node from the queue and use it as the next starting place
- Run time is often written as `O(|E| + |V|)` number of edges + vertices
