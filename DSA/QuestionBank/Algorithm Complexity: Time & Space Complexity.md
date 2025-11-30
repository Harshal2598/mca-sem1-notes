# 📘 Algorithm Complexity: Time & Space Complexity

Algorithm complexity is used to measure **how efficient** an algorithm is.  
The two most important measures are:

- **Time Complexity** → How fast an algorithm runs  
- **Space Complexity** → How much memory an algorithm uses  

---

# 1️⃣ Time Complexity

## 📌 Definition  
Time Complexity is the **total time taken by an algorithm to run**, based on the size of input `n`.

It does **not** measure time in seconds.  
Instead, it measures the **number of basic operations** an algorithm performs.

### ✔ Why Time Complexity is Important?
- Helps compare two algorithms  
- Predicts performance for large inputs  
- Determines which algorithm is more efficient  

---

## ⭐ Types of Time Complexity (Big-O Notation)

| Complexity | Name | Example |
|------------|------|---------|
| **O(1)** | Constant Time | Accessing array element |
| **O(log n)** | Logarithmic | Binary search |
| **O(n)** | Linear | Simple loop |
| **O(n log n)** | Linearithmic | Merge sort, Quick sort (avg) |
| **O(n²)** | Quadratic | Nested loops |
| **O(2ⁿ)** | Exponential | Subset generation |
| **O(n!)** | Factorial | Traveling Salesman (brute force) |

### ✔ Example (Linear Time)
```c
for(int i = 0; i < n; i++) {
    // 1 operation repeated n times
}
Time Complexity = O(n)

2️⃣ Space Complexity
📌 Definition
Space Complexity is the amount of memory an algorithm uses:

Input space

Auxiliary (extra) space

Temporary variables, arrays, recursive stack

✔ Why Space Complexity Matters?
Important for memory-limited devices

Helps choose memory-efficient algorithms

Helps avoid stack overflow in recursion

⭐ Types of Space Usage
1. Fixed Space (Constant Space)
Memory used does not change with input size.

Example:

c
Copy code
int x, y;
Space = O(1)

2. Variable Space
Memory grows with input.

Example:

c
Copy code
int arr[n];
Space = O(n)

⭐ Examples
✔ Example 1: Algorithm using O(1) Space
c
Copy code
int sum = 0;   // only one variable
✔ Example 2: Algorithm using O(n) Space
c
Copy code
int arr[n];    // array size depends on input
✔ Example 3: Recursive Function (Stack Space)
c
Copy code
void recursion(int n){
    if(n == 0) return;
    recursion(n-1);
}
Uses O(n) stack memory.

🧠 Time vs Space Complexity (Comparison)
Feature	Time Complexity	Space Complexity
Measures	Execution time	Memory usage
Affects	Speed	Memory footprint
Notation	Big-O	Big-O
Goal	Reduce execution time	Reduce extra memory
Example	O(n log n)	O(n)

📝 Short Exam Answer
Algorithm complexity describes the efficiency of an algorithm.
Time Complexity measures how much time an algorithm takes as input size increases.
Space Complexity measures how much memory an algorithm uses during execution.

Time complexity uses Big-O notation like O(1), O(n), O(n²), O(log n).
Space complexity includes memory required for variables, arrays, and recursion stack, such as O(1) and O(n).

Efficient algorithms aim to reduce both time and space usage.
