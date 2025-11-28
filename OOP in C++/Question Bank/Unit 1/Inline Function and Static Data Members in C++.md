# Inline Function and Static Data Members in C++

Below are two important concepts of C++ used for performance improvement and memory management.

---

# 1️⃣ Inline Function

An **inline function** is a function in which the compiler copies the function code directly at the place where it is called.  
This **avoids the overhead of function calls**, making the program faster.

### ✔ When to use?
- For **short, simple functions**
- To reduce function-call overhead

### ✔ Syntax
```cpp
inline returnType functionName(parameters) {
    // code
}
```

---

## ✔ Example: Inline Function
```cpp
#include <iostream>
using namespace std;

inline int square(int x) {   // inline keyword
    return x * x;
}

int main() {
    cout << "Square = " << square(5);
    return 0;
}
```

### ✔ How it works?
Instead of calling square(5), the compiler replaces it with:
```
cout << "Square = " << (5 * 5);
```

### ✔ Advantage
- Faster execution because no function call happens  
- Best for small one-line functions

---

# 2️⃣ Static Data Members

A **static data member** belongs to the **class** rather than any individual object.  
It is **shared by all objects** of the class.

### ✔ Key Points
- Memory is allocated **only once**
- All objects share the same variable
- Must be defined outside the class

---

## ✔ Example: Static Data Member
```cpp
#include <iostream>
using namespace std;

class Student {
public:
    int roll;
    static int count;   // static variable declaration

    Student(int r) {
        roll = r;
        count++;        // increments shared variable
    }

    void show() {
        cout << "Roll: " << roll 
             << ", Total Students: " << count << endl;
    }
};

// static variable definition (outside class)
int Student::count = 0;

int main() {
    Student s1(1);
    Student s2(2);

    s1.show();
    s2.show();

    return 0;
}
```

### ✔ Output
```
Roll: 1, Total Students: 1
Roll: 2, Total Students: 2
```

### ✔ Explanation
- `count` is shared by all objects  
- Each time a new object is created → count increases  
- Only **one memory location** for `count`

---

# ⭐ Summary Table

| Concept | Meaning | Memory Usage | Example |
|--------|---------|---------------|---------|
| Inline Function | Function expanded at call site | Faster (no call overhead) | `inline int square(int x)` |
| Static Data Member | Shared variable for all objects | One copy for entire class | `static int count;` |

---

# 🎯 Conclusion
- **Inline functions** increase speed by eliminating function calls.  
- **Static data members** reduce memory usage by sharing one variable across all objects.

Both concepts help in writing **efficient and optimized** C++ programs.
