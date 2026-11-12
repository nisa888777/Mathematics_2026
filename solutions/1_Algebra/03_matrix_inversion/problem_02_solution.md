# Exercise 2. Formula for a $2 \times 2$ Matrix

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

For a general $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\\ c & d \end{pmatrix}$, the inverse exists if and only if $\det(M) = ad - bc \neq 0$, and is given by the formula:

$$
M^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\\ -c & a \end{pmatrix}
$$

---

### 1. Compute the Determinant of $A$

Identifying the entries $a = 3$, $b = 2$, $c = 5$, and $d = 4$:

$$
\det(A) = (3)(4) - (2)(5) = 12 - 10 = 2
$$

Since $\det(A) = 2 \neq 0$, the inverse matrix $A^{-1}$ exists.

---

### 2. Apply the $2 \times 2$ Inverse Formula

Substituting the entries and $\det(A) = 2$ into the formula:

$$
A^{-1} = \frac{1}{2} \begin{pmatrix} 4 & -2 \\\ -5 & 3 \end{pmatrix} = \begin{pmatrix} 2 & -1 \\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}
$$

---

### 3. Verify the Result

To verify that $A^{-1}$ is correct, we compute the matrix product $A A^{-1}$:

$$
A A^{-1} = \begin{pmatrix} 3 & 2 \\\ 5 & 4 \end{pmatrix} \begin{pmatrix} 2 & -1 \\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}
$$

Evaluating each entry:

* Row 1, Column 1: $(3)(2) + (2)\left(-\frac{5}{2}\right) = 6 - 5 = 1$
* Row 1, Column 2: $(3)(-1) + (2)\left(\frac{3}{2}\right) = -3 + 3 = 0$
* Row 2, Column 1: $(5)(2) + (4)\left(-\frac{5}{2}\right) = 10 - 10 = 0$
* Row 2, Column 2: $(5)(-1) + (4)\left(\frac{3}{2}\right) = -5 + 6 = 1$

$$
A A^{-1} = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} = I
$$

Since the product yields the $2 \times 2$ identity matrix $I$, the computed inverse is verified.

---

### Conclusion

* The determinant is $\det(A) = 2$.
* The inverse matrix is $A^{-1} = \begin{pmatrix} 2 & -1 \\\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}$.
