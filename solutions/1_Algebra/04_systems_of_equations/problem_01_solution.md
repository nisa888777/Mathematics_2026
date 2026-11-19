# Exercise 1. Definition of the Inverse

## Question

For

$$A = \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & -1 \\\ -1 & 2 \end{pmatrix}$$

check, without using a formula, whether $B = A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

---

## Solution

We are given the $2 \times 2$ matrices:

$$A = \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & -1 \\\ -1 & 2 \end{pmatrix}$$

---

### 1. Compute $AB$

Multiplying $A$ by $B$ on the right:

$$AB = \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\\ -1 & 2 \end{pmatrix} = \begin{pmatrix} (2)(1) + (1)(-1) & (2)(-1) + (1)(2) \\\ (1)(1) + (1)(-1) & (1)(-1) + (1)(2) \end{pmatrix} = \begin{pmatrix} 2 - 1 & -2 + 2 \\\ 1 - 1 & -1 + 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} = I$$

---

### 2. Compute $BA$

Multiplying $B$ by $A$ on the right:

$$BA = \begin{pmatrix} 1 & -1 \\\ -1 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix} = \begin{pmatrix} (1)(2) + (-1)(1) & (1)(1) + (-1)(1) \\\ (-1)(2) + (2)(1) & (-1)(1) + (2)(1) \end{pmatrix} = \begin{pmatrix} 2 - 1 & 1 - 1 \\\ -2 + 2 & -1 + 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} = I$$

---

### 3. Relation to the Definition of the Inverse

By definition, an $n \times n$ matrix $A$ is invertible if there exists an $n \times n$ matrix $B$ such that:

$$AB = I \quad \text{and} \quad BA = I$$

where $I$ is the $n \times n$ identity matrix. Because both products equal the $2 \times 2$ identity matrix $I$, $B$ satisfies the exact definition of the inverse of $A$. By the uniqueness of the matrix inverse, we conclude that $B = A^{-1}$.

---

### Conclusion

* Both $AB = I$ and $BA = I$ hold.
* Therefore, by the definition of a matrix inverse, **$B = A^{-1}$**.
