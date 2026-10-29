# Exercise 2. Determinant of a 3x3 Matrix

**Given Matrix:**

$$
A = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & 3 & 4 \\\ 2 & 1 & 5 \end{pmatrix}
$$

---

### **1. Compute $\det(A)$ Using Sarrus' Rule**

To apply Sarrus' rule, append the first two columns to the right of the matrix:

$$
\begin{matrix}
1 & 2 & -1 & 1 & 2 \\\
0 & 3 & 4 & 0 & 3 \\\
2 & 1 & 5 & 2 & 1
\end{matrix}
$$

* **Sum of the products along the main diagonals (top-left to bottom-right):**

$$
D_1 = (1)(3)(5) + (2)(4)(2) + (-1)(0)(1)
$$

$$
D_1 = 15 + 16 + 0 = 31
$$

* **Sum of the products along the anti-diagonals (bottom-left to top-right):**

$$
D_2 = (2)(3)(-1) + (1)(4)(1) + (5)(0)(2)
$$

$$
D_2 = -6 + 4 + 0 = -2
$$

* **Determinant calculation:**

$$
\det(A) = D_1 - D_2 = 31 - (-2) = 31 + 2 = 33
$$

---

### **2. Verification Using Determinant Properties (Cofactor Expansion)**

We can check the result by expanding along the first column, which contains a zero to simplify calculation:

$$
\det(A) = a_{11} C_{11} + a_{21} C_{21} + a_{31} C_{31}
$$

$$
\det(A) = 1 \cdot \det\begin{pmatrix} 3 & 4 \\\ 1 & 5 \end{pmatrix} - 0 \cdot \det\begin{pmatrix} 2 & -1 \\\ 1 & 5 \end{pmatrix} + 2 \cdot \det\begin{pmatrix} 2 & -1 \\\ 3 & 4 \end{pmatrix}
$$

Evaluating the $2 \times 2$ determinants:

* **First minor:**

$$
\det\begin{pmatrix} 3 & 4 \\\ 1 & 5 \end{pmatrix} = (3)(5) - (4)(1) = 15 - 4 = 11
$$

* **Second minor:**

$$
\det\begin{pmatrix} 2 & -1 \\\ 3 & 4 \end{pmatrix} = (2)(4) - (-1)(3) = 8 - (-3) = 11
$$

Substituting these back into the expansion:

$$
\det(A) = 1(11) - 0 + 2(11) = 11 + 22 = 33
$$

Both methods confirm that:

$$
\det(A) = 33
$$
