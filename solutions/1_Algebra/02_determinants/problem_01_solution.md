# Exercise 1. Determinant of a 2x2 Matrix

**Recall:**  
For any $2 \times 2$ matrix:

$$
M = \begin{pmatrix} a & b \\\ c & d \end{pmatrix}
$$

its determinant is calculated as:

$$
\det(M) = ad - bc
$$

A matrix is invertible if and only if its determinant is non-zero ($\det(M) \neq 0$).

---

### **1. Compute the Determinants**

* **First Matrix:**

$$
A = \begin{pmatrix} 3 & -2 \\\ 5 & 4 \end{pmatrix}
$$

$$
\det(A) = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22
$$

* **Second Matrix:**

$$
B = \begin{pmatrix} 1 & 7 \\\ 2 & 14 \end{pmatrix}
$$

$$
\det(B) = (1)(14) - (7)(2) = 14 - 14 = 0
$$

---

### **2. Invertibility and Justification**

* **Matrix $A$:**  
  Since $\det(A) = 22 \neq 0$, matrix $A$ is **invertible** (non-singular). Its columns (and rows) are linearly independent.

* **Matrix $B$:**  
  Since $\det(B) = 0$, matrix $B$ is **not invertible** (singular). Notice that the second row is an exact scalar multiple of the first row:

$$
\text{Row}_2 = 2 \times \text{Row}_1
$$

which makes the rows linearly dependent.
