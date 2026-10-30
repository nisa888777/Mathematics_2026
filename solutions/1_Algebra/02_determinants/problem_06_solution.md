# Exercise 6. Parameter and Invertibility

## Question

For

$$
A(t) = \begin{pmatrix} t & 1 \\\ 2 & t \end{pmatrix}
$$

find all values of $t$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

---

## Solution

A square matrix is invertible if and only if its determinant is non-zero ($\det \neq 0$). Conversely, a matrix is **not invertible** (singular) if and only if its determinant equals zero:

$$
\det(A(t)) = 0
$$

---

### 1. Compute the Determinant $\det(A(t))$

For a $2 \times 2$ matrix:

$$
A(t) = \begin{pmatrix} t & 1 \\\ 2 & t \end{pmatrix}
$$

the determinant is computed using the standard formula $\det = ad - bc$:

$$
\det(A(t)) = (t)(t) - (1)(2) = t^2 - 2
$$

---

### 2. Find Values of $t$ Where $A(t)$ is Not Invertible

To find the values of $t$ for which $A(t)$ is not invertible, we set the determinant to zero:

$$
t^2 - 2 = 0
$$

Solving for $t$:

$$
t^2 = 2 \implies t = \pm\sqrt{2}
$$

Thus, the matrix is not invertible when $t = \sqrt{2}$ or $t = -\sqrt{2}$.

---

### 3. Relation to the Determinant Being Zero

The relationship between invertibility and the determinant being zero can be understood geometrically and algebraically:

* **Algebraic perspective:**  
  The inverse of a $2 \times 2$ matrix $M$:

$$
M = \begin{pmatrix} a & b \\\ c & d \end{pmatrix}
$$

  is given by:

$$
M^{-1} = \frac{1}{\det(M)} \begin{pmatrix} d & -b \\\ -c & a \end{pmatrix}
$$

  When $\det(A(t)) = 0$, computing $A(t)^{-1}$ would require dividing by zero, which is undefined. Therefore, the matrix cannot have an inverse.

* **Linear dependence:**  
  When $t = \pm\sqrt{2}$, the rows (and columns) of $A(t)$ become linearly dependent:
  * For $t = \sqrt{2}$, row 2 is a scalar multiple of row 1: $\sqrt{2} \cdot (\sqrt{2}, 1) = (2, \sqrt{2})$.
  * Linearly dependent rows mean the transformation collapses the 2D plane into a 1D line (area scale factor $= 0$), which cannot be inverted.

---

### Conclusion

* **Values of $t$ for which $A(t)$ is not invertible:**

$$
t = \sqrt{2} \quad \text{and} \quad t = -\sqrt{2}
$$

* The matrix is not invertible precisely at these values because the determinant vanishes ($\det(A(t)) = 0$), meaning the matrix is singular and cannot be inverted.
