# Class and Object in C++

In Object-Oriented Programming (OOP), **class** and **object** are the two most fundamental concepts.  
A class is a blueprint, while an object is a real entity created from that blueprint.

---

# 1️⃣ What is a Class?

A **class** is a **user-defined data type** that contains:
- **Data members** (variables)
- **Member functions** (methods)

It acts as a **template / blueprint** for creating objects.

### ✔ Characteristics of a Class
- Defines how an object will look and behave  
- Does not occupy memory until an object is created  
- Helps achieve **encapsulation** (bundling data + functions)

### ✔ Syntax
```cpp
class ClassName {
public:
    // data members
    // member functions
};
```

---

## ✔ Example of a Class
```cpp
class Student {
public:
    string name;
    int age;

    void study() {
        cout << name << " is studying" << endl;
    }
};
```

---

# 2️⃣ What is an Object?

An **object** is an **instance** of a class.  
When a class is declared, no memory is allocated, but when an object is created, memory is assigned.

### ✔ Characteristics of an Object
- Real-world entity  
- Has **state (data)** and **behavior (functions)**  
- Uses the class definition to store data and perform actions  

### ✔ Syntax
```cpp
ClassName objectName;
```

---

## ✔ Example of an Object
```cpp
int main() {
    Student s1;       // s1 is an object
    s1.name = "Harshal";
    s1.age = 20;

    s1.study();       // calling member function
    return 0;
}
```

### ✔ Output
```
Harshal is studying
```

---

# ⭐ Real-Life Example

| Class | Object |
|-------|---------|
| Car | Honda, BMW, Mahindra |
| Student | Harshal, Riya, Arjun |
| Mobile | iPhone, Samsung, OnePlus |

---

# ⭐ Difference Between Class and Object

| Class | Object |
|-------|---------|
| Blueprint or template | Real entity created from the class |
| No memory allocated | Memory allocated |
| Logical representation | Physical representation |
| Contains definitions | Contains actual values |

---

# 🎯 Conclusion

- **Class** gives the **structure**.  
- **Object** is the **living instance** of that structure.  
Together, they form the foundation of **Object-Oriented Programming (OOP)**.

