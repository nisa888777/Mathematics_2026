# Exercise 2. Addition and Scalar Multiplication

**Given Matrices:**

$$
A = \begin{pmatrix} 1 & 2 \\\ -1 & 3 \end{pmatrix}, \quad B = \begin{pmatrix} 4 & -2 \\\ 0 & 5 \end{pmatrix}
$$

Both matrices have dimension $2 \times 2$.

---

### **1. Matrix Addition ($A + B$)**

To add two matrices of the same dimension, we add corresponding entries:

$$
A + B = \begin{pmatrix} 1 + 4 & 2 + (-2) \\\ -1 + 0 & 3 + 5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\\ -1 & 8 \end{pmatrix}
$$

---

### **2. Matrix Subtraction ($A - B$)**

To subtract matrices, we subtract the entries of matrix $B$ from matrix $A$:

$$
A - B = \begin{pmatrix} 1 - 4 & 2 - (-2) \\\ -1 - 0 & 3 - 5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\\ -1 & -2 \end{pmatrix}
$$

---

### **3. Scalar Multiplication and Combination ($3A - 2B$)**

First, multiply matrix $A$ by $3$ and matrix $B$ by $2$:

$$
3A = 3 \begin{pmatrix} 1 & 2 \\\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\\ -3 & 9 \end{pmatrix}
$$

$$
2B = 2 \begin{pmatrix} 4 & -2 \\\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 8 & -4 \\\ 0 & 10 \end{pmatrix}
$$

Now compute $3A - 2B$:

$$
3A - 2B = \begin{pmatrix} 3 - 8 & 6 - (-4) \\\ -3 - 0 & 9 - 10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\\ -3 & -1 \end{pmatrix}
$$

---

### **4. Dimension Compatibility Explanation**

Matrix addition is performed entry-by-entry. An entry at row $i$ and column $j$ in matrix $A$ can only be combined with the entry at the exact same position $(i, j)$ in matrix $B$. If the dimensions differ, corresponding entries do not exist, making the operation mathematically undefined.
