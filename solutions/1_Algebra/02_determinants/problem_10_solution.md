# Exercise 10. Detecting Dependence

## Question

Without carrying out a full determinant calculation, explain why

$$
\det \begin{pmatrix} 1 & 2 & 3 \\\ 2 & 4 & 6 \\\ 0 & 1 & 5 \end{pmatrix} = 0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

---

## Solution

Let the given matrix be denoted as $A$:

$$
A = \begin{pmatrix} 1 & 2 & 3 \\\ 2 & 4 & 6 \\\ 0 & 1 & 5 \end{pmatrix}
$$

Let the rows of matrix $A$ be represented as row vectors:
* $\mathbf{r}_1 = (1, 2, 3)$
* $\mathbf{r}_2 = (2, 4, 6)$
* $\mathbf{r}_3 = (0, 1, 5)$

---

### 1. Identifying the Specific Linear Dependence

Comparing row 1 ($\mathbf{r}_1$) and row 2 ($\mathbf{r}_2$):

$$
\mathbf{r}_2 = 2 \cdot \mathbf{r}_1
$$

Explicitly:

$$
(2, 4, 6) = 2 \cdot (1, 2, 3) = (2(1), 2(2), 2(3))
$$

This can be expressed as a non-trivial linear combination equaling the zero vector:

$$
2\mathbf{r}_1 - \mathbf{r}_2 + 0\mathbf{r}_3 = \mathbf{0}
$$

Therefore, the rows of matrix $A$ are **linearly dependent**.

---

### 2. Connection to the Determinant Being Zero

A fundamental property of determinants states that if one row of a matrix is a scalar multiple of another row (or if the rows are linearly dependent), the determinant of the matrix is zero:

* Applying the elementary row operation $R_2 \to R_2 - 2R_1$:

$$
\det(A) = \det \begin{pmatrix} 1 & 2 & 3 \\\ 2 - 2(1) & 4 - 2(2) & 6 - 2(3) \\\ 0 & 1 & 5 \end{pmatrix} = \det \begin{pmatrix} 1 & 2 & 3 \\\ 0 & 0 & 0 \\\ 0 & 1 & 5 \end{pmatrix}
$$

* Since row 2 becomes entirely zero, expanding along the second row immediately yields:

$$
\det(A) = 0
$$

---

### 3. Connection with Noninvertibility

The linear dependence of the rows directly implies that matrix $A$ is **not invertible** (singular) for the following reasons:

* **Rank and Dimension:**  
  Because row 2 provides no independent dimension, the row space has dimension $\operatorname{rank}(A) \le 2 < 3$. For a $3 \times 3$ matrix to be invertible, it must have full rank ($\operatorname{rank}(A) = 3$).
* **Kernel / Null Space:**  
  A rank deficiency means there exist non-zero vectors $\mathbf{x} \neq \mathbf{0}$ such that $A\mathbf{x} = \mathbf{0}$. Therefore, the linear transformation is not injective (one-to-one).
* **Invertibility Theorem:**  
  According to the Invertible Matrix Theorem, a square matrix $A$ is invertible if and only if $\det(A) \neq 0$. Since $\det(A) = 0$, $A$ cannot possess an inverse matrix $A^{-1}$.

---

### Conclusion

* **Specific Row Dependence:** Row 2 is exactly twice row 1 ($\mathbf{r}_2 = 2\mathbf{r}_1$).
* **Determinant:** $\det(A) = 0$ without a full calculation, because two rows are proportional.
* **Noninvertibility:** Because the rows are linearly dependent, the matrix has $\operatorname{rank}(A) < 3$ and $\det(A) = 0$, making the matrix singular (noninvertible).
