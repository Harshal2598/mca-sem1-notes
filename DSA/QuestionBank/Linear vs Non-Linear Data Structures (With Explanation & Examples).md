# 📦 Linear vs Non-Linear Data Structures (With Explanation & Examples)

## 🧠 What is a Data Structure?
A **Data Structure** is a way of organizing and storing data so operations like searching, inserting, and deleting can be performed efficiently.

---

# 🔹 Linear Data Structures

A **Linear Data Structure** arranges data **sequentially**, meaning elements are stored one after another.

### ✔ Characteristics
- Elements are arranged in a **single level**.
- Traversal is **one-by-one**.
- Simple implementation.

### ✔ Examples
- Array  
- Linked List  
- Stack  
- Queue  

---

## ✔ Example of a Linear Data Structure  
### **1. Stack (LIFO – Last In, First Out)**

A stack allows insertion and deletion at **one end only** (top).

### **Operations**
- `push()` → Insert element  
- `pop()` → Remove top element  
- `peek()` → Look at top element  

### **Real-Life Example**
Stack of plates – last plate placed is the first removed.

### **Simple C++ Example**
```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> s;
    s.push(10);
    s.push(20);
    s.push(30);

    cout << "Top Element: " << s.top();  // 30
}
🔹 Non-Linear Data Structures
A Non-Linear Data Structure arranges data hierarchically or interconnected, not in sequence.

✔ Characteristics
Data is stored on multiple levels.

Traversal is complex.

Represents relationships.

✔ Examples
Tree

Graph

Heap

Trie

✔ Example of a Non-Linear Data Structure
1. Tree (Hierarchical Structure)
A tree contains nodes connected in a parent-child relationship.

Binary Tree Example
markdown
Copy code
     10
    /  \
   5    20
Real-Life Example
Computer File System

Organization hierarchy

Simple C++ Example
cpp
Copy code
struct Node {
    int data;
    Node* left;
    Node* right;
};
📝 Short Exam Answer
Linear Data Structures store data in a sequential order.
Examples: Array, Linked List, Stack, Queue.

Non-Linear Data Structures store data in a hierarchical or network model.
Examples: Tree, Graph, Heap.

Example of Linear DS → Stack, which works on LIFO principle.
Example of Non-Linear DS → Tree, where data is stored in parent-child levels.
