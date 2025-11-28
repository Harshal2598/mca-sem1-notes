# Call by Value and Call by Reference in C++

In C++, functions can receive arguments in two ways:

1. **Call by Value**  
2. **Call by Reference**

These determine **how data is passed** to a function and **whether the original value changes**.

---

# 1️⃣ Call by Value

In **call by value**, a **copy** of the actual variable is passed to the function.  
Changes made inside the function **do NOT affect** the original variable.

### ✔ Example: Call by Value
```cpp
#include <iostream>
using namespace std;

void changeValue(int x) {
    x = 50;  // modifies only the local copy
}

int main() {
    int a = 10;
    changeValue(a);
    cout << "Value of a: " << a;  // remains 10
    return 0;
}
```

### ✔ Output
```
Value of a: 10
```

### ✔ Key Point
> Changes are NOT reflected in the original variable.

---

# 2️⃣ Call by Reference

In **call by reference**, the **address** of the variable is passed.  
Changes made inside the function **DO affect** the original variable.

C++ allows reference passing using **& symbol**.

### ✔ Example: Call by Reference
```cpp
#include <iostream>
using namespace std;

void changeValue(int &x) {  // x refers to a
    x = 50;  
}

int main() {
    int a = 10;
    changeValue(a);
    cout << "Value of a: " << a;  // becomes 50
    return 0;
}
```

### ✔ Output
```
Value of a: 50
```

### ✔ Key Point
> Changes made inside the function are reflected in the original variable.

---

# 📌 Summary Table

| Method | What is passed? | Original Value Changes? | Use Case |
|--------|----------------|---------------------------|-----------|
| Call by Value | Copy of variable | ❌ No | When original data must stay safe |
| Call by Reference | Address/reference | ✔ Yes | When original data must be modified |

---

# ⭐ Conclusion
- **Call by Value** → Safe, original value unchanged  
- **Call by Reference** → Efficient when modifying original value  

Both methods help programmers control how data is shared between functions.

