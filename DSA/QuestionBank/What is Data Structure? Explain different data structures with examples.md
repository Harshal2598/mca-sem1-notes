“What is Data Structure? Explain different data structures with examples.”
# 📦 What is a Data Structure?

A **Data Structure** is a way of organizing, storing, and managing data so that it can be used efficiently.  
It defines how data is arranged in memory and what operations can be performed on it.

### ✔ Simple Definition:
> A data structure is a specialized format for storing and organizing data so that it can be accessed and processed efficiently.

Examples of operations:  
- Searching  
- Insertion  
- Deletion  
- Sorting  
- Traversing  

---

# 🧰 Types of Data Structures (With Examples)

Data structures are mainly divided into **Linear** and **Non-Linear** types.

---

# 1️⃣ Linear Data Structures

These store data in a **sequential** manner.

---

## **A. Array**
A collection of elements of the **same type**, stored in **continuous memory**.

### Example:
```cpp
int arr[5] = {10, 20, 30, 40, 50};

B. Linked List

A sequence of nodes where each node contains:

Data

Pointer to next node

Example Node:
struct Node {
    int data;
    Node* next;
};


Types:

Singly Linked List

Doubly Linked List

Circular Linked List

C. Stack

A LIFO (Last In, First Out) structure.
Insertion & deletion happen at top.

Operations:

push()

pop()

peek()

Example:

Stack of books: last placed = first removed.

D. Queue

A FIFO (First In, First Out) structure.
Insertion at rear, deletion at front.

Operations:

enqueue()

dequeue()

Example:

People standing in a queue at a ticket counter.

2️⃣ Non-Linear Data Structures

Data is stored in hierarchical or interconnected form.

A. Tree

A hierarchical DS with a root node.

Example:

Binary Tree:

    10
   /  \
  5    20


Types:

Binary Tree

Binary Search Tree (BST)

AVL Tree

Heap

B-Trees

B. Graph

A set of nodes (vertices) and edges connecting them.
Represents relationships.

Example:
A --- B
|   / |
|  /  |
C --- D


Used in:

Social networks

Google Maps

Networking

3️⃣ Hash-Based Data Structures
A. Hash Table / Hash Map

Stores data in key-value pairs using a hash function.

Example:
unordered_map<string, int> marks;
marks["Harshal"] = 95;


Used for fast searching (O(1) average time).

4️⃣ Other Important Data Structures
A. Heap

A specialized tree-based structure:

Max Heap → root has highest value

Min Heap → root has lowest value

Used in:

Priority queues

Dijkstra’s algorithm

B. Trie (Prefix Tree)

Used for storing strings efficiently.

Example:

Autocomplete systems use tries.

📝 Short Exam Answer

A data structure is a method of organizing and storing data so operations like searching, inserting, and deleting can be done efficiently.

Common data structures:

Array: Stores elements in continuous memory.

Linked List: Stores data in nodes linked by pointers.

Stack: LIFO structure.

Queue: FIFO structure.

Tree: Hierarchical structure.

Graph: Network of connected nodes.

Hash Table: Stores key-value pairs for fast search.

Heap & Trie: Used in priority processing and string operations.
