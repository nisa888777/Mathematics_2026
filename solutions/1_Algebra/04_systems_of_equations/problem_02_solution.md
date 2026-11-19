# Exercise 2. Formula for a 2×2 Matrix

## Question

Find the inverse of

$$
A = \begin{pmatrix} 3 & 2 \\\ 5 & 4 \end{pmatrix}
$$

using the formula for a $2 \times 2$ matrix. At the end, check the result by computing one product with $A$.

---

## Solution

We are given the $2 \times 2$ matrix:

$$
A = \begin{pmatrix} 3 & 2 \\\ 5 & 4 \end{pmatrix}
$$

---

### 1. Apply the $2 \times 2$ Inverse Formula

For a general $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\\ c & d \end{pmatrix}$, the inverse exists if $\det(A) = ad - bc \neq 0$ and is given by:

$$
A^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\\ -c & a \end{pmatrix}
$$

First, we compute the determinant of $A$:

$$
\det(A) = (3)(4) - (2)(5) = 12 - 10 = 2
$$

Since $\det(A) = 2 \neq 0$, $A^{-1}$ exists. Substituting $a = 3$, $b = 2$, $c = 5$, and $d = 4$ into the formula:

$$
A^{-1} = \frac{1}{2} \begin{pmatrix} 4 & -2 \\\ -5 & 3 \end{pmatrix} = \begin{pmatrix} 2 & -1 \\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}
$$

---

### 2. Check the Result by Computing $A A^{-1}$

We multiply $A$ by $A^{-1}$ to verify that the product equals the identity matrix $I$:

$$
A A^{-1} = \begin{pmatrix} 3 & 2 \\\ 5 & 4 \end{pmatrix} \begin{pmatrix} 2 & -1 \\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix} = \begin{pmatrix} (3)(2) + (2)\left(-\frac{5}{2}\right) & (3)(-1) + (2)\left(\frac{3}{2}\right) \\\ (5)(2) + (4)\left(-\frac{5}{2}\right) & (5)(-1) + (4)\left(\frac{3}{2}\right) \end{pmatrix} = \begin{pmatrix} 6 - 5 & -3 + 3 \\\ 10 - 10 & -5 + 6 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} = I
$$

Since $A A^{-1} = I$, the inverse matrix is verified.

---

### Conclusion

* The determinant of $A$ is $\det(A) = 2 \neq 0$.
* The inverse matrix is:

$$
A^{-1} = \begin{pmatrix} 2 & -1 \\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}
$$
