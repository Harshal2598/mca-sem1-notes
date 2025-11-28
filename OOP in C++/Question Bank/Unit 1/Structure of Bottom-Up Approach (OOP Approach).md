# Structure of Bottom-Up Approach (OOP Approach)

The **Bottom-Up Approach** is the programming style used in **Object-Oriented Programming (OOP)**.  
In this model, the program is developed by **building small components (objects)** first and then combining them to form a complete system.

It is opposite to the **Top-Down Approach**, which starts from the main function and breaks into smaller parts.

---

# ⭐ Key Idea
> Start by creating **objects**, **classes**, and **small modules** → combine them to build a complete program.

---

# ✔ Structure of Bottom-Up Approach

The structure generally follows these steps:

---

## 1️⃣ Identify Real-World Entities  
- First step is to understand the real-world problem.  
- Identify **objects** that represent entities (e.g., Student, Car, Employee).

Example:  
In a school system → Student, Teacher, Class, Marks.

---

## 2️⃣ Define Classes  
- Create classes for each entity.  
- Each class contains **data members** (attributes) and **member functions** (behaviors).

Example:
```cpp
class Student {
    int roll;
    string name;
    void display();
};
```

---

## 3️⃣ Create Objects From Classes  
- Objects are created from classes.  
- Each object represents one real-world instance.

Example:
```cpp
Student s1, s2;
```

---

## 4️⃣ Build Small Modules  
- Each object performs a small task.  
- These tasks are independent and reusable.

Example:
- Student object handles marks  
- Teacher object handles attendance  

Each module works on its own.

---

## 5️⃣ Establish Interaction Between Objects  
- Objects communicate using **methods**, **messages**, and **function calls**.

Example:
```cpp
s1.display();
teacher.giveMarks(s1);
```

---

## 6️⃣ Combine All Modules  
- After developing small components, they are combined to create the complete system.  
- This makes the program **modular**, **scalable**, and **easy to maintain**.

---

# 📌 Example Diagram (Bottom-Up Flow)

```
Objects  →  Classes  →  Modules  →  Subsystems  →  Final System
```

---

# ⭐ Advantages of Bottom-Up Approach

- Encourages **code reusability**
- More **modular and flexible**
- Easy to **maintain and update**
- Real-world modelling becomes simple
- Enhances **data security** using encapsulation

---

# 🎯 Conclusion
The **Bottom-Up Approach** builds programs by first designing the smallest units (classes & objects) and then assembling them into a complete application.  
It is the foundation of **Object-Oriented Programming (OOP)** and widely used in modern software development.

