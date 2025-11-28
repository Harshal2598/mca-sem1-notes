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
# Call by Address in C++ (Using Pointers)

**Call by Address** is a method of passing arguments to a function where the **address of the variable** is passed instead of the value.  
This is done using **pointers**.

Because the function receives the **memory address**, any changes made inside the function **directly modify the original variable**.

---

# ✔ How Call by Address Works
- A pointer parameter receives the address of a variable.
- Using `*` (dereference operator), the function can access and modify the actual variable.
- Changes reflect in the original memory location.

---

# ✔ Syntax
```cpp
void functionName(int *ptr) {
    // function body
}
```

---

# ✔ Example: Call by Address Using Pointers
```cpp
#include <iostream>
using namespace std;

// function using pointer to modify value
void updateValue(int *p) {
    *p = 50;   // modifies original value
}

int main() {
    int x = 10;

    updateValue(&x);   // passing address of x

    cout << "Value of x: " << x;  // Output: 50
    return 0;
}
```

---

# ✔ Explanation

### In `main()`:
```cpp
int x = 10;
updateValue(&x);
```
- `&x` passes the **address** of `x`.

### In `updateValue()`:
```cpp
void updateValue(int *p) {
    *p = 50;
}
```
- `p` stores the address of `x`.  
- `*p` accesses the value at that address.  
- Changing `*p` modifies the original variable.

---

# 📌 When to Use Call by Address?

- When you want the function to **modify the original variable**.
- When passing large objects (more efficient).
- Useful in swapping, updating values, dynamic memory handling.

---

# ⭐ Example: Swapping Values Using Call by Address
```cpp
void swapValues(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 10, y = 20;

    swapValues(&x, &y);

    cout << "x = " << x << ", y = " << y;  // Output: x = 20, y = 10
}
```

---

# 🎯 Summary

| Method | What is Passed? | Can Change Original Value? |
|--------|------------------|----------------------------|
| Call by Value | Copy of value | ❌ No |
| Call by Address | Address (pointer) | ✔ Yes |
| Call by Reference | Alias | ✔ Yes |

**Call by Address** using pointers is powerful because it gives the function **direct access** to original variables.



