# Inline Function and Static Data Member in C++

Inline functions and static data members are important features in C++ that help in improving performance and memory efficiency.

---

# 1️⃣ Inline Function

An **inline function** is a function in which the compiler replaces the **function call** with the **actual function code** at compile time.

### ✔ Why Inline?
- Avoids the overhead of a function call  
- Makes execution faster  
- Best for **small functions** (1–3 lines)

### ✔ Syntax
```cpp
inline returnType functionName(parameters) {
    // code
}
```

---

## ✔ Example of Inline Function
```cpp
#include <iostream>
using namespace std;

inline int square(int x) {
    return x * x;
}

int main() {
    cout << "Square of 5 = " << square(5);
    return 0;
}
```

### ✔ Output
```
Square of 5 = 25
```

### ✔ Explanation
- When we write `square(5)`, the compiler replaces it with `5 * 5`.  
- No function call happens → faster execution.

---

# 2️⃣ Static Data Member

A **static data member** belongs to the **class**, not to individual objects.

### ✔ Features
- Only **one copy** is created, shared by all objects  
- Stored in **static memory**  
- Must be defined **outside the class**  
- Useful for counting objects, common data, etc.

---

## ✔ Example of Static Data Member
```cpp
#include <iostream>
using namespace std;

class Student {
public:
    int roll;
    static int count;   // declaration

    Student(int r) {
        roll = r;
        count++;        // increments shared static variable
    }

    void display() {
        cout << "Roll = " << roll 
             << ", Total Students = " << count << endl;
    }
};

// definition of static member
int Student::count = 0;

int main() {
    Student s1(1);
    Student s2(2);

    s1.display();
    s2.display();

    return 0;
}
```

---

### ✔ Output
```
Roll = 1, Total Students = 1
Roll = 2, Total Students = 2
```

### ✔ Explanation
- `count` is shared among all objects.  
- Each time a new object is created, `count` increases.  
- Only **one memory location** is used for `count`, even if there are many objects.

---

# ⭐ Summary Table

| Feature | Inline Function | Static Data Member |
|--------|------------------|---------------------|
| Purpose | Faster execution | Shared data between objects |
| Memory | No extra memory | Single memory for class |
| Defined | Inside class | Declared in class, defined outside |
| Best Use | Small functions | Counting objects, common data |

---

# 🎯 Conclusion
- **Inline functions** improve speed by eliminating function call overhead.  
- **Static data members** save memory and allow sharing information between all objects of a class.  
Both concepts help in creating **efficient and optimized** C++ programs.
