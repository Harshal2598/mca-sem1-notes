# Program: Add Two Complex Numbers Using Friend Function & Copy Constructor

```cpp
#include <iostream>
using namespace std;

class Complex {
private:
    int real, imag;

public:
    // Default constructor
    Complex() {
        real = 0;
        imag = 0;
    }

    // Parameterized constructor
    Complex(int r, int i) {
        real = r;
        imag = i;
    }

    // Copy constructor
    Complex(const Complex &c) {
        real = c.real;
        imag = c.imag;
    }

    // Friend function to add two Complex numbers
    friend Complex add(Complex c1, Complex c2);

    // Function to display result
    void display() {
        cout << real << " + " << imag << "i" << endl;
    }
};

// Friend function definition
Complex add(Complex c1, Complex c2) {
    Complex temp;
    temp.real = c1.real + c2.real;
    temp.imag = c1.imag + c2.imag;
    return temp;        // returns a Complex object → invokes copy constructor
}

int main() {
    Complex c1(3, 4);      // 3 + 4i
    Complex c2(5, 6);      // 5 + 6i

    Complex sum = add(c1, c2);   // using friend function

    cout << "First number: ";
    c1.display();

    cout << "Second number: ";
    c2.display();

    cout << "Sum of two complex numbers: ";
    sum.display();

    return 0;
}
```

---

# ⭐ Explanation

### ✔ 1. Constructors
- **Default constructor** initializes values to 0.
- **Parameterized constructor** initializes with given values.
- **Copy constructor** copies values from one object to another.

### ✔ 2. Friend Function
`friend Complex add(Complex c1, Complex c2);`  
- Accesses private members `real` and `imag`.
- Adds corresponding parts of two objects.

### ✔ 3. Copy Constructor Use
When we return `temp` from `add()`,  
the object is **copied**, invoking the **copy constructor**.

---

# ✔ Output

```
First number: 3 + 4i
Second number: 5 + 6i
Sum of two complex numbers: 8 + 10i
```

---

If you want, I can also write:
✔ Operator overloading for complex numbers  
✔ Program to subtract/multiply/divide complex numbers  
✔ `.md` notes for constructors, copy constructors, friend functions & classes
