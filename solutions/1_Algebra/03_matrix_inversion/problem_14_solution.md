# Exercise 14. A Matrix That Is Its Own Inverse

## Question

Assume that a square matrix $A$ satisfies

$$
A^2 = I.
$$

Show that

$$
A^{-1} = A.
$$

Then give an example of a $2 \times 2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

---

## Solution

### 1. Proof That $A^{-1} = A$

By definition, a square matrix $A$ is invertible if there exists a matrix $B$ of the same size such that:

$$
AB = I \quad \text{and} \quad BA = I
$$

When such a matrix $B$ exists, it is unique and is denoted as $B = A^{-1}$.

We are given that $A^2 = I$, which can be written as:

$$
A \cdot A = I
$$

Comparing this directly with the definition of the matrix inverse ($AB = BA = I$), we see that the matrix $B = A$ satisfies both $AB = I$ and $BA = I$. By the uniqueness of the inverse matrix, it follows immediately that:

$$
A^{-1} = A
$$

---

### 2. Example of a $2 \times 2$ Matrix ($A \neq I, -I$)

Consider the $2 \times 2$ reflection (or permutation) matrix:

$$
A = \begin{pmatrix} 0 & 1 \\\ 1 & 0 \end{pmatrix}
$$

Clearly, $A \neq I = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix}$ and $A \neq -I = \begin{pmatrix} -1 & 0 \\\ 0 & -1 \end{pmatrix}$.

*(Note: Geometrically, $A$ reflects points across the line $y = x$; applying the reflection twice returns every point to its original position.)*

---

### 3. Verification by Multiplication

We compute $A^2 = A \cdot A$:

$$
A^2 = \begin{pmatrix} 0 & 1 \\\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 \\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (0)(0) + (1)(1) & (0)(1) + (1)(0) \\\ (1)(0) + (0)(1) & (1)(1) + (0)(0) \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} = I
$$

Since $A^2 = I$, we confirm that $A^{-1} = A$.

---

### Conclusion

* Because $A \cdot A = I$ matches the definition of an inverse, any involutory matrix satisfying $A^2 = I$ is its own inverse ($A^{-1} = A$).
* The matrix $A = \begin{pmatrix} 0 & 1 \\\ 1 & 0 \end{pmatrix}$ is distinct from $I$ and $-I$ and satisfies $A^2 = I$.
