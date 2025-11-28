# Access Specifiers in C++

Access specifiers (also called access modifiers) in C++ define **how the members of a class (variables & functions)** can be accessed from outside the class.

C++ provides **three** access specifiers:

1. `public`
2. `private`
3. `protected`

These control **visibility** and **access level** of class members.

---

# 1️⃣ public

Members declared as **public** are accessible:
- Inside the class  
- Outside the class  
- Using objects  

### ✔ Example
```cpp
#include <iostream>
using namespace std;

class Demo {
public:  
    int x;  // public member

    void show() {
        cout << "Value of x = " << x;
    }
};

int main() {
    Demo obj;
    obj.x = 10;     // allowed
    obj.show();     // allowed
}
```

### ✔ Output
```
Value of x = 10
```

---

# 2️⃣ private

Members declared as **private** are accessible:
- Only inside the class  
- NOT accessible outside the class  
- NOT accessible using objects  

### ✔ Example
```cpp
#include <iostream>
using namespace std;

class Demo {
private:
    int secret;  // private member

public:
    void setData(int s) {
        secret = s; // allowed
    }

    void show() {
        cout << "Secret = " << secret;
    }
};

int main() {
    Demo obj;
    // obj.secret = 20;  ❌ ERROR - private member
    obj.setData(20);    // allowed
    obj.show();
}
```

### ✔ Output
```
Secret = 20
```

---

# 3️⃣ protected

Members declared as **protected** are accessible:
- Inside the class  
- In derived (child) classes  
- NOT accessible using objects  

### ✔ Example (with inheritance)
```cpp
#include <iostream>
using namespace std;

class Base {
protected:
    int value;  // protected member
};

class Derived : public Base {
public:
    void setValue(int v) {
        value = v;  // allowed (inside derived class)
    }

    void show() {
        cout << "Value = " << value;
    }
};

int main() {
    Derived obj;
    // obj.value = 10; ❌ ERROR - protected member
    obj.setValue(10);
    obj.show();
}
```

### ✔ Output
```
Value = 10
```

---

# ⭐ Summary Table

| Access Specifier | Access Inside Class | Access Outside Class | Access in Derived Class |
|------------------|----------------------|------------------------|---------------------------|
| **public** | ✔ Yes | ✔ Yes | ✔ Yes |
| **private** | ✔ Yes | ❌ No | ❌ No |
| **protected** | ✔ Yes | ❌ No | ✔ Yes |

---

# 🎯 Conclusion
Access specifiers in C++ control the visibility of class members and help achieve **encapsulation**, which is one of the key pillars of OOP.  
They ensure data security and proper structure in object-oriented programming.

