# Exercise 1. Determinant of a 2×2 Matrix

## Question

Compute

$$
\det \begin{pmatrix} 3 & -2 \\\ 5 & 4 \end{pmatrix}, \qquad \det \begin{pmatrix} 1 & 7 \\\ 2 & 14 \end{pmatrix}.
$$

Which matrix is invertible? Justify your answer.

---

## Solution

For a $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\\ c & d \end{pmatrix}$, the determinant is given by:

$$
\det(M) = ad - bc
$$

---

### 1. First Matrix

Let $A = \begin{pmatrix} 3 & -2 \\\ 5 & 4 \end{pmatrix}$. Computing its determinant:

$$
\det(A) = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22
$$

---

### 2. Second Matrix

Let $B = \begin{pmatrix} 1 & 7 \\\ 2 & 14 \end{pmatrix}$. Computing its determinant:

$$
\det(B) = (1)(14) - (7)(2) = 14 - 14 = 0
$$

---

### 3. Invertibility and Justification

A square matrix is invertible if and only if its determinant is non-zero ($\det \neq 0$).

* **Matrix $A = \begin{pmatrix} 3 & -2 \\\ 5 & 4 \end{pmatrix}$ is invertible** because $\det(A) = 22 \neq 0$. Its columns (and rows) are linearly independent, so a unique inverse matrix $A^{-1}$ exists.
* **Matrix $B = \begin{pmatrix} 1 & 7 \\\ 2 & 14 \end{pmatrix}$ is not invertible (singular)** because $\det(B) = 0$. Notice that the second row is twice the first row ($2 \cdot (1, 7) = (2, 14)$), meaning the rows are linearly dependent and the matrix collapses space into a line.

---

### Conclusion

* $\det \begin{pmatrix} 3 & -2 \\\ 5 & 4 \end{pmatrix} = 22$ — **Invertible** ($\det \neq 0$).
* $\det \begin{pmatrix} 1 & 7 \\\ 2 & 14 \end{pmatrix} = 0$ — **Not invertible** ($\det = 0$).
