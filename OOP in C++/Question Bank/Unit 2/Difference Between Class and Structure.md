# Difference Between Class and Structure in C++

Both **class** and **structure** are user-defined data types in C++.  
However, they differ in terms of access control, features, and usage.

---

# ⭐ Key Differences Between Class and Structure

| Feature | Structure (`struct`) | Class (`class`) |
|---------|----------------------|------------------|
| **Default Access Specifier** | `public` | `private` |
| **Data Hiding** | Less secure | Highly secure |
| **Functions Inside** | Allowed | Allowed |
| **Inheritance** | Supported | Supported |
| **Object-Oriented Programming** | Not fully OOP | Fully supports OOP concepts |
| **Use Case** | Used for simple data grouping | Used for complex data & behaviors |
| **Memory Allocation** | Similar to class | Similar to struct |
| **Keyword** | `struct` | `class` |
| **Constructors/Destructors** | Allowed | Allowed |
| **Access Modifiers** | public, private, protected | public, private, protected |

---

# ✔ Explanation of Differences

## 1️⃣ Default Access Specifier
- In **structures**, members are **public** by default.  
- In **classes**, members are **private** by default.

### Example:
```cpp
struct A {   // public by default
    int x;
};

class B {    // private by default
    int y;
};
```

---

## 2️⃣ Data Hiding (Security)
- Structure provides **low-level** data hiding.  
- Class provides **strong** data hiding using private & protected specifiers.

---

## 3️⃣ Object-Oriented Features
- Structure supports OOP features, but **usually used for data-holding only**.  
- Class is used for **full OOP programming** (encapsulation, inheritance, polymorphism, abstraction).

---

## 4️⃣ Usage
- **Structure:**  
  Good for grouping related variables.  
  Example: Student record, coordinates.

- **Class:**  
  Good for modelling real-world entities with data + behavior.  
  Example: Car, Bank Account, Employee.

---

# ✔ Example Showing Difference

```cpp
#include <iostream>
using namespace std;

struct Student {
    int roll;          // public
    void show() {
        cout << "Roll: " << roll;
    }
};

class Employee {
private:
    int salary;        // private

public:
    void setSalary(int s) {
        salary = s;
    }
    void show() {
        cout << "Salary: " << salary;
    }
};
```

---

# 🎯 Summary

- **Class** → Default private, more secure, best for OOP  
- **Structure** → Default public, simple data grouping  
- Both support functions, constructors, destructors, inheritance, etc.  
- Class is preferred for **complex applications**, struct for **simple data storage**.

