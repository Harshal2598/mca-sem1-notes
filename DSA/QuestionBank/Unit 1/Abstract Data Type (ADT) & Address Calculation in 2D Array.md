# Explain the term ADT with example. Consider the integer array arr[30] [40] declared in C
,base address of array is 700, find the address of element arr[12][20] using row major and
column major address implementation.

# 📘 Abstract Data Type (ADT) & Address Calculation in 2D Array

## 1️⃣ What is ADT (Abstract Data Type)?

An **Abstract Data Type (ADT)** is a *logical description* of a data structure that specifies:

- **What operations** it can perform  
- **What behavior** it must show  

…but **does NOT specify how it is implemented internally** in memory or code.

### ✔ Simple Definition
> ADT defines *what a data structure does*, not *how it is implemented*.

### ✔ Example of ADT
**Stack ADT** supports:
- push(x)
- pop()
- peek()
- isEmpty()

But ADT does NOT say:
- whether stack is implemented using array or linked list  
- how memory is managed internally  

Thus, ADT gives *behavior*, not *implementation*.

---

# 2️⃣ Address Calculation in 2D Array

Given:

int arr[30][40];
Base Address = 700
Element to find = arr[12][20]

yaml
Copy code

### Indexing assumption:
C language uses **0-based indexing**  
So:
- Row index = 12  
- Column index = 20  

### Sizes:
Rows = 30  
Columns = 40  
Assume **int = 2 bytes** (standard assumption unless mentioned)

---

# 📌 2D Array Address Formula

## 🟦 **Row Major Order (C Language Default)**

Address = Base + [ (row_index * total_columns) + column_index ] * size

shell
Copy code

### Substitute values:
Base = 700
row_index = 12
column_index = 20
total_columns = 40
size = 2 bytes

yaml
Copy code

### Step-by-step:
1. row_index * total_columns =  
   12 × 40 = 480  

2. 480 + column_index =  
   480 + 20 = 500  

3. 500 × size =  
   500 × 2 = 1000  

4. Address =  
   700 + 1000 = **1700**

### ✅ **Row Major Address of arr[12][20] = 1700**

---

## 🟩 **Column Major Order**

Address = Base + [ (column_index * total_rows) + row_index ] * size

shell
Copy code

### Substitute values:
Base = 700
column_index = 20
row_index = 12
total_rows = 30
size = 2 bytes

yaml
Copy code

### Step-by-step:
1. column_index * total_rows =  
   20 × 30 = 600  

2. 600 + row_index =  
   600 + 12 = 612  

3. 612 × size =  
   612 × 2 = 1224  

4. Address =  
   700 + 1224 = **1924**

### ✅ **Column Major Address of arr[12][20] = 1924**

---

# 📝 Final Answers

| Order | Address of arr[12][20] |
|-------|--------------------------|
| **Row Major** | **1700** |
| **Column Major** | **1924** |
