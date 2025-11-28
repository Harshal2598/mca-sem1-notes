# Data Types in C++

C++ provides different data types to store different kinds of values such as integers, characters, decimals, and Boolean values.  
They are mainly classified into **three categories**:

1. **Primitive (Built-in) Data Types**  
2. **User-Defined Data Types**  
3. **Derived Data Types**

---

# 1️⃣ Primitive (Built-in) Data Types

These are basic data types provided by C++.

| Data Type | Size | Example | Description |
|-----------|------|---------|-------------|
| `int` | 4 bytes | `int a = 10;` | Stores whole numbers (positive/negative) |
| `char` | 1 byte | `char c = 'A';` | Stores a single character |
| `float` | 4 bytes | `float x = 3.14;` | Stores decimal numbers (single precision) |
| `double` | 8 bytes | `double y = 10.567;` | Stores double-precision decimals |
| `bool` | 1 byte | `bool flag = true;` | Stores true/false values |
| `void` | — | `void func()` | Represents empty return type |
| `wchar_t` | 2–4 bytes | `wchar_t wc = L'A';` | Stores wide characters (Unicode) |

### ✔ Brief Explanation:
- **int** → Used for integers like 10, -5  
- **char** → Stores single alphabet or symbol  
- **float/double** → Used for decimal values  
- **bool** → Used in conditions (true/false)  
- **void** → Functions that return nothing  
- **wchar_t** → Unicode/extended characters  

---

# User-Defined Data Types in C++

User-defined data types are data types that are **created by the programmer**.  
They allow you to define your own structure of data based on the needs of the program.  
These types make C++ more flexible and powerful.

C++ provides the following user-defined data types:

---

# 1️⃣ `struct` (Structure)

A structure groups **different types of variables** under one name.

### Example:
```cpp
struct Student {
    int roll;
    char name[20];
    float marks;
};
```

### ✔ Use:
- When you want to store **different types of data together**
- Common in databases, records, objects, etc.

---

# 2️⃣ `class`

A class is the **most important user-defined type in C++**.  
It is used to create **objects** and supports **OOP concepts** like encapsulation, inheritance, and polymorphism.

### Example:
```cpp
class Car {
public:
    int speed;
    void drive() {
        cout << "Driving";
    }
};
```

### ✔ Use:
- Building objects  
- Object-oriented programming  
- Large applications (games, software, systems)

---

# 3️⃣ `enum` (Enumeration)

An enumeration is a set of **named integer constants**.

### Example:
```cpp
enum Color { Red, Green, Blue };
```

### ✔ Use:
- Useful when a variable should have **only fixed values**
- Improves code readability

---

# 4️⃣ `typedef`

`typedef` is used to **give another name (alias)** to an existing data type.

### Example:
```cpp
typedef int marks;
marks m1 = 90;
```

### ✔ Use:
- To create short and meaningful names  
- In complex declarations (pointers, structures)

---

# 5️⃣ `union`

A union allows storing **different data types in the same memory location**.  
Only one member can contain a value at a time.

### Example:
```cpp
union Data {
    int n;
    float f;
    char ch;
};
```

### ✔ Use:
- Memory-efficient programs  
- Embedded systems  
- Situations where you need one value at a time  

---

# ⭐ Summary Table

| User-Defined Data Type | Description |
|------------------------|-------------|
| `struct` | Group of different data types |
| `class` | Blueprint for objects (OOP) |
| `enum` | Named constants |
| `typedef` | Type alias |
| `union` | Shared memory for different variables |

---

# 🎯 Conclusion

User-defined data types give C++ its flexibility and power.  
They allow programmers to create customized data structures, organize code, and build complex applications using object-oriented techniques.



---

# 3️⃣ Derived Data Types

These are built using primitive types.

| Data Type | Example | Description |
|-----------|---------|-------------|
| Array | `int arr[10];` | Collection of similar data items |
| Pointer | `int *ptr;` | Stores memory address |
| Function | `int sum(int a, int b);` | Reusable block of code |
| Reference | `int &ref = x;` | Alias for another variable |

### ✔ Brief Explanation:
- **Array** → Store multiple values of same type  
- **Pointer** → Used for dynamic memory & address handling  
- **Functions** → For code reuse  
- **Reference** → Alternate name for a variable  

---

# ⭐ Summary

| Category | Examples | Purpose |
|----------|----------|----------|
| Primitive | int, char, float, double, bool | Basic data storage |
| User-Defined | struct, class, enum, union | Custom data structures |
| Derived | array, pointer, function, reference | Advanced programming needs |

---

# 🎯 Conclusion
C++ offers a rich set of data types that help store different types of values efficiently. These data types form the foundation of all C++ programs and allow programmers to manage memory, structure code, and build complex applications.
