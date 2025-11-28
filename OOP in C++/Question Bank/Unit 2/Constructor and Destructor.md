# C++ Program to Explain Constructor and Destructor

```cpp
#include <iostream>
using namespace std;

class Demo {
public:
    // Constructor
    Demo() {
        cout << "Constructor Called: Object Created!" << endl;
    }

    // Member function
    void show() {
        cout << "Inside show() function!" << endl;
    }

    // Destructor
    ~Demo() {
        cout << "Destructor Called: Object Destroyed!" << endl;
    }
};

int main() {
    Demo obj; // Object created → Constructor will be called automatically

    obj.show(); // Member function call

    return 0; // End of the program → Destructor will be called automatically
}
```

---

# ✔ Output
```
Constructor Called: Object Created!
Inside show() function!
Destructor Called: Object Destroyed!
```

---

# ⭐ Explanation

- **Constructor**
  - Special function with the same name as the class
  - Automatically called when an object is created
  - Used for initialization

- **Destructor**
  - Begins with **~** (tilde)
  - Automatically called when the object goes out of scope or program ends
  - Used for cleanup (freeing memory, closing files)

---

| Feature | Constructor | Destructor |
|--------|-------------|------------|
| When called | Object creation | Object destruction |
| Name | Same as class name | Same as class name with `~` |
| Parameters | Allowed | Not allowed |
| Overloading | Yes | No |
| Purpose | Initialization | Cleanup |

---

# 🎯 Conclusion
This program demonstrates how constructor initializes the object upon creation, and destructor releases resources when the object is destroyed.  
These are essential features of **Object-Oriented Programming** in C++.
