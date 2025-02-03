This episode explores how data is stored and organized in computer memory using **data structures**, moving beyond simple variables to more complex arrangements.

## 🧱 Basic Data Structures

- **Arrays (Lists/Vectors)**: A series of values stored in memory.
    
    - Instead of saving single values, an array stores a series of values.
    - Each value is accessed using an **index**, starting from 0 in most languages.
    - For example, in an array `j`, `j` refers to the first value, `j` to the second, and so on.
    - Arrays are stored contiguously in memory. For example, if an array starts at memory location 1000, the subsequent values are stored at 1001, 1002, etc..
    - Arrays are versatile and widely used, with many built-in functions for sorting etc..
- **Strings**: Arrays of characters (letters, numbers, punctuation).
    
    - Strings are stored in memory similarly to arrays, with each character occupying a memory location.
    - A **null character** (binary value 0) marks the end of a string in memory. This is important for functions like `print quote`, which need to know when to stop outputting characters.
    - Many functions specifically handle strings, like **concatenation** (`strcat`), which combines two strings.
- **Matrices**: Arrays of arrays, used to represent two-dimensional data like grids or pixels.
    
    - A 3x3 matrix can be visualized as an array of size 3, where each element is an array of size 3.
    - To access an element, two indexes are needed: one for the "row" and one for the "column", like `J`.
    - Matrices are not limited to two dimensions, and can be extended to more dimensions, like 5-dimensional matrices.

## 📦 Compound Data Structures

- **Structs**: Bundles of related variables of different types.
    
    - A struct can group variables like a bank account number and balance.
    - Arrays of structs can be created, and are also stored contiguously in memory.
    - Accessing an element of a struct array means first getting the struct and then pulling specific data from it.
    - Arrays of structs are of fixed size and cannot easily be extended.
- **Linked Lists**: A flexible data structure made of nodes that each point to the next node in the list.
    
    - Each **node** is a struct containing a value and a **pointer** to the next node in memory.
    - Nodes in a linked list are not necessarily stored next to each other in memory and can be created at different times.
    - The `next` pointer in a node contains the memory location of the next node.
    - A **null pointer** (value of 0) indicates the end of the linked list.
    - Linked lists allow for dynamic resizing, unlike arrays, and can be easily reordered, trimmed, split, and reversed.

## 🥞 Abstract Data Structures built on Linked Lists

- **Queues**: Follow the **FIFO** (First-In-First-Out) principle, like a line at a post office.
    
    - A pointer, for example "post office queue", points to the first node in a linked list.
    - Items are removed ("dequeued") from the front, by reading the next pointer to update the queue.
    - New items are added ("enqueued") to the end of the list by traversing to the end and adding the new item there.
- **Stacks**: Follow the **LIFO** (Last-In-First-Out) principle, like a stack of pancakes.
    
    - New items are added ("pushed") to the top of the stack.
    - Items are removed ("popped") from the top of the stack.
- **Trees**: Hierarchical data structure, where each node can have multiple "child" nodes.
    
    - The topmost node is called the **root**, nodes hanging below are **children**, nodes above children are **parents**, and nodes at the end of branches are called **leaf nodes**.
    - A **binary tree** is a type of tree where each node has up to two children.
    - In trees, there is a one-way path from root to leaves.
- **Graphs**: Nodes with many pointers, but without the parent-child relationships of trees.
    
    - Graphs allow for arbitrary connections, including loops.
    - They can represent networks like cities connected by roads.

## 🧠 Conclusion

- Data structures are fundamental for organizing and manipulating data in computer science.
- Programmers use existing data structures, and combine and customize them to solve complex problems.
- Many programming languages have libraries full of ready-made data structures, like the C++ Standard Template Library and Java Class Library, meaning programmers don't have to implement them from scratch.

This episode explains many of the core data structures used in computer science, emphasizing how they allow us to manage and interact with data efficiently.