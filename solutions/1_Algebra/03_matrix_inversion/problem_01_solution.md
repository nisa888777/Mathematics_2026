# Exercise 1. Definition of the Inverse

## Question

For

$$
A = \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & -1 \\\ -1 & 2 \end{pmatrix}
$$

check, without using a formula, whether $B = A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

---

## Solution

We are given two $2 \times 2$ matrices:

$$
A = \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & -1 \\\ -1 & 2 \end{pmatrix}
$$

By definition, a square matrix $B$ is the inverse of a square matrix $A$ (denoted $B = A^{-1}$) if and only if:

$$
AB = BA = I
$$

where $I = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix}$ is the $2 \times 2$ identity matrix.

---

### 1. Compute $AB$

$$
AB = \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\\ -1 & 2 \end{pmatrix}
$$

Evaluating each entry:

* Row 1, Column 1: $(2)(1) + (1)(-1) = 2 - 1 = 1$
* Row 1, Column 2: $(2)(-1) + (1)(2) = -2 + 2 = 0$
* Row 2, Column 1: $(1)(1) + (1)(-1) = 1 - 1 = 0$
* Row 2, Column 2: $(1)(-1) + (1)(2) = -1 + 2 = 1$

$$
AB = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} = I
$$

---

### 2. Compute $BA$

$$
BA = \begin{pmatrix} 1 & -1 \\\ -1 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix}
$$

Evaluating each entry:

* Row 1, Column 1: $(1)(2) + (-1)(1) = 2 - 1 = 1$
* Row 1, Column 2: $(1)(1) + (-1)(1) = 1 - 1 = 0$
* Row 2, Column 1: $(-1)(2) + (2)(1) = -2 + 2 = 0$
* Row 2, Column 2: $(-1)(1) + (2)(1) = -1 + 2 = 1$

$$
BA = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} = I
$$

---

### 3. Relation to the Definition of the Inverse

Since both matrix products $AB$ and $BA$ yield the $2 \times 2$ identity matrix $I$, matrix $B$ satisfies the exact algebraic definition of the multiplicative inverse of $A$.

---

### Conclusion

* Both $AB = I$ and $BA = I$ hold.
* Therefore, **$B = A^{-1}$**.
