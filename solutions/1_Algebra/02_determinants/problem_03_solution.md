# Exercise 3. Swapping Two Rows

**Given Matrix:**

$$
A = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 3 & 1 \\\ 2 & 1 & 1 \end{pmatrix}
$$

---

### **1. Compute $\det(A)$**

Expanding along the first row:

$$
\det(A) = 1 \cdot \det\begin{pmatrix} 3 & 1 \\\ 1 & 1 \end{pmatrix} - 2 \cdot \det\begin{pmatrix} 0 & 1 \\\ 2 & 1 \end{pmatrix} + 0 \cdot \det\begin{pmatrix} 0 & 3 \\\ 2 & 1 \end{pmatrix}
$$

Evaluating the $2 \times 2$ determinants:

* **First minor:**

$$
\det\begin{pmatrix} 3 & 1 \\\ 1 & 1 \end{pmatrix} = (3)(1) - (1)(1) = 3 - 1 = 2
$$

* **Second minor:**

$$
\det\begin{pmatrix} 0 & 1 \\\ 2 & 1 \end{pmatrix} = (0)(1) - (1)(2) = 0 - 2 = -2
$$

Substituting these back into the expansion:

$$
\det(A) = 1(2) - 2(-2) + 0 = 2 + 4 = 6
$$

---

### **2. Form Matrix $B$ and Predict $\det(B)$**

Matrix $B$ is obtained by swapping the first and second rows of $A$ ($R_1 \leftrightarrow R_2$):

$$
B = \begin{pmatrix} 0 & 3 & 1 \\\ 1 & 2 & 0 \\\ 2 & 1 & 1 \end{pmatrix}
$$

* **Prediction Using Determinant Properties:**  
  Swapping two rows of a matrix multiplies its determinant by $-1$:

$$
\det(B) = -\det(A) = -6
$$

---

### **3. Verify $\det(B)$ by Direct Calculation**

Expanding along the first row of $B$:

$$
\det(B) = 0 \cdot \det\begin{pmatrix} 2 & 0 \\\ 1 & 1 \end{pmatrix} - 3 \cdot \det\begin{pmatrix} 1 & 0 \\\ 2 & 1 \end{pmatrix} + 1 \cdot \det\begin{pmatrix} 1 & 2 \\\ 2 & 1 \end{pmatrix}
$$

Evaluating the $2 \times 2$ determinants:

* **First non-zero minor:**

$$
\det\begin{pmatrix} 1 & 0 \\\ 2 & 1 \end{pmatrix} = (1)(1) - (0)(2) = 1 - 0 = 1
$$

* **Second non-zero minor:**

$$
\det\begin{pmatrix} 1 & 2 \\\ 2 & 1 \end{pmatrix} = (1)(1) - (2)(2) = 1 - 4 = -3
$$

Substituting these back into the expansion:

$$
\det(B) = 0 - 3(1) + 1(-3) = -3 - 3 = -6
$$

---

### **Conclusion**

Direct computation confirms that:

$$
\det(B) = -6 = -\det(A)
$$

This verifies that swapping two rows reverses the sign of the determinant.
