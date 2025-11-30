# 📦 Abstract Data Type (ADT) & Array as ADT

# 1️⃣ What is an Abstract Data Type (ADT)?

An **Abstract Data Type (ADT)** is a *theoretical model* that defines:
- **What operations** can be performed  
- **What behavior** the data type shows  

…but **does NOT specify how the operations are implemented** internally.

### ✔ Simple Definition
> ADT describes *what a data type does*, not *how it does it*.

### ✔ Example:
- Stack ADT → push(), pop(), peek()  
- Queue ADT → enqueue(), dequeue()  

The ADT only tells **operations**, not the programming logic behind them.

---

# 2️⃣ Array as an Abstract Data Type (Array ADT)

An **Array as an ADT** defines a structure that stores **fixed-size, sequential elements** and supports a set of operations.

### ✔ Array ADT = A model of how an array behaves.

The **implementation** (C++, Java, Python) may differ,  
but the **behavior (ADT operations)** remains the same.

---

## 🧰 Operations of Array ADT

### **1. Insert(index, value)**
Add a value at a specific index.

### **2. Delete(index)**
Remove an element from a given index.

### **3. Get(index)**
Return the value stored at an index.

### **4. Set(index, value)**
Change the value at an index.

### **5. Search(value)**
Find the index of a value.

### **6. Traverse()**
Visit all elements one by one.

---

## 📊 Array ADT Representation

Array: A[0…n-1]

Operations:

A.get(i)

A.set(i, value)

A.insert(i, value)

A.delete(i)

A.search(value)

A.traverse()

csharp
Copy code

---

# ✔ Example of Array ADT Operations (C++)

```cpp
#include <iostream>
using namespace std;

class ArrayADT {
public:
    int arr[5];

    void set(int index, int value) {
        arr[index] = value;
    }

    int get(int index) {
        return arr[index];
    }
};

int main() {
    ArrayADT a;
    a.set(0, 10);
    a.set(1, 20);

    cout << a.get(0) << endl; // 10
    cout << a.get(1) << endl; // 20
}
📝 Short Exam Answer
ADT (Abstract Data Type) is a mathematical model that specifies what operations a data type must support without describing how they are implemented.

Array as ADT supports operations like:

Insert

Delete

Get

Set

Search

Traverse

Array ADT defines how arrays behave logically, independent of programming language implementation.
