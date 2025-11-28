# Friend Function and Friend Class in C++

In C++, the concepts of **friend function** and **friend class** allow controlled access to the private and protected members of a class.  
They help when two classes or external functions need to work closely together.

---

# 1️⃣ Friend Function

A **friend function** is a function that is **not a member of a class**, but it is allowed to access the **private and protected members** of that class.

### ✔ Why do we need a friend function?
- When we want an outside function to access private data  
- When two classes need to share data  
- Useful for operator overloading  

### ✔ Syntax
```cpp
class ClassName {
    friend returnType functionName(parameters);
};
```

---

## ✔ Example of Friend Function
```cpp
#include <iostream>
using namespace std;

class Demo {
private:
    int x;

public:
    Demo(int a) {
        x = a;
    }

    // friend function declaration
    friend void show(Demo d);
};

// friend function definition
void show(Demo d) {
    cout << "Value of x = " << d.x;   // access private member
}

int main() {
    Demo obj(10);
    show(obj);
    return 0;
}
```

### ✔ Output
```
Value of x = 10
```

### ✔ Explanation
- `show()` is **not a member** of class Demo.
- Still, it can access private variable `x` because it is declared as a *friend*.

---

# 2️⃣ Friend Class

A **friend class** allows **all member functions** of one class to access the **private and protected members** of another class.

### ✔ Why do we need a friend class?
- When two classes work closely together  
- When one class needs full access to another class  
- Useful in operator overloading, complex data structures (tree, list)

### ✔ Syntax
```cpp
class A {
    friend class B;
};
```

---

## ✔ Example of Friend Class
```cpp
#include <iostream>
using namespace std;

class A {
private:
    int secret;

public:
    A(int s) {
        secret = s;
    }

    friend class B;   // B is a friend class
};

class B {
public:
    void showSecret(A obj) {
        cout << "Secret = " << obj.secret;  // can access private data
    }
};

int main() {
    A a1(100);
    B b1;
    b1.showSecret(a1);

    return 0;
}
```

### ✔ Output
```
Secret = 100
```

---

# ⭐ Difference Between Friend Function and Friend Class

| Feature | Friend Function | Friend Class |
|---------|-----------------|--------------|
| Access | Only that function gets access | All functions of the friend class get access |
| Usage | Selective access | Full class-to-class access |
| Declaration | `friend void show();` | `friend class B;` |
| Control | More controlled | Less controlled |

---

# 🎯 Summary

- **Friend Function** → A non-member function that can access private members.  
- **Friend Class** → Gives full access of one class to another class.  
- Both are used for:
  - Data sharing  
  - Operator overloading  
  - Close interaction between classes  

They break the strict encapsulation *only when necessary*, making them powerful tools in C++.

