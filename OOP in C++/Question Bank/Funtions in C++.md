# Functions in C++ (6 Marks)

A **function** in C++ is a block of code designed to perform a specific task. It helps in code reusability, modularity, readability, and makes large programs easier to manage.

Functions allow us to divide a program into smaller parts, making it easier to debug and maintain.

---

## ✔ Features of Functions
- Improve code **reusability**  
- Make code **modular** and structured  
- Reduce duplication  
- Increase readability  
- Allow **divide-and-conquer** programming  

---

# Types of Functions in C++

## 1️⃣ **Built-in Functions**
Functions provided by C++ libraries.

Example:
```cpp
#include <iostream>
#include <cmath>

int main() {
    std::cout << sqrt(16);  // sqrt() is a built-in function
}
```

---

## 2️⃣ **User-Defined Functions**
Functions created by the programmer.

### Syntax:
```cpp
return_type functionName(parameters) {
    // function body
}
```

---

# ✔ Example of a User-Defined Function
```cpp
#include <iostream>
using namespace std;

// Function to add two numbers
int add(int a, int b) {
    return a + b;
}

int main() {
    int result = add(5, 10);  
    cout << "Sum = " << result;
    return 0;
}
```

### Output:
```
Sum = 15
```

---

# ✔ Function Components

| Component | Meaning |
|----------|---------|
| Return Type | Type of value returned (int, float, void, etc.) |
| Function Name | Identifier for the function |
| Parameters | Input values to the function |
| Function Body | Statements executed when called |
| Return Statement | Sends result back to caller |

---

# ✔ Advantages of Using Functions
- Avoids repetition of code  
- Makes code shorter and cleaner  
- Easy to debug and update  
- Allows teamwork (multiple people can work on different functions)  
- Improves program structure  

---

# ⭐ Conclusion
Functions are one of the most important concepts in C++. They make programs modular, reusable, and easier to understand. Both built-in and user-defined functions help in writing clean and efficient code, making them essential for programming and exams.

