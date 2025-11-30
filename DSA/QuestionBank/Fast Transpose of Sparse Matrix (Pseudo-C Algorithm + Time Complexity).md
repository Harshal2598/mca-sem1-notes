#Q. Write a pseudo C algorithm for fast transpose of sparse matrix. Also mention the time
complexity.

# ⚡ Fast Transpose of Sparse Matrix (Pseudo-C Algorithm + Time Complexity)

The **Fast Transpose Algorithm** is an optimized version of simple transpose used for **Sparse Matrices in Triplet Form**.  
It reduces unnecessary scanning and achieves **O(n + columns)** time.

A sparse matrix in 3-tuple form looks like:

Row | Col | Value

yaml
Copy code

---

# ✅ Pseudo-C Algorithm for Fast Transpose of Sparse Matrix

Given sparse matrix `A` with:
- `A[0][0] = rows`
- `A[0][1] = cols`
- `A[0][2] = numNonZero`

Goal → Produce transpose matrix `B`.

---

## 🔹 **FAST TRANSPOSE ALGORITHM**

```c
FastTranspose(A, B)
{
    int rowsA = A[0][0];
    int colsA = A[0][1];
    int num = A[0][2];

    // Step 1: If matrix empty, just copy first row
    B[0][0] = colsA;
    B[0][1] = rowsA;
    B[0][2] = num;

    if (num > 0)
    {
        // Step 2: Count number of elements in each column
        int count[colsA];
        for (int i = 0; i < colsA; i++)
            count[i] = 0;

        for (int i = 1; i <= num; i++)
            count[A[i][1]]++;

        // Step 3: Calculate starting position of each column in B
        int index[colsA];
        index[0] = 1;
        for (int i = 1; i < colsA; i++)
            index[i] = index[i-1] + count[i-1];

        // Step 4: Place elements directly in the correct positions
        for (int i = 1; i <= num; i++)
        {
            int col = A[i][1];
            int pos = index[col];

            B[pos][0] = A[i][1];   // row becomes col
            B[pos][1] = A[i][0];   // col becomes row
            B[pos][2] = A[i][2];   // value same

            index[col]++;          // move to next free slot
        }
    }
}
📌 Explanation of Steps
Step 1 – Copy dimensions
Transpose has:

rows ↔ columns swapped

Step 2 – Count non-zero elements in each column
This helps in placing transposed elements directly.

Step 3 – Compute starting positions
Starting index of each column in output array.

Step 4 – Place elements
Elements placed in correct position without scanning entire matrix.

🧠 Time Complexity
✔ Naive Transpose:
scss
Copy code
O(rows × columns)
✔ Fast Transpose:
scss
Copy code
O(numNonZero + columns)
This is significantly faster for large sparse matrices.

📝 Final Exam Answer (Short)
Fast Transpose uses:

Count occurrences of each column

Compute starting index

Insert each element in correct position

Time Complexity = O(N + C)
Where:

N = number of non-zero elements

C = number of columns
