# Exercise 6. Solving a System Using the Inverse

## Question

Solve

$$
Ax = b,
$$

where

$$
A = \begin{pmatrix} 2 & 1 \\\ 1 & 3 \end{pmatrix}, \qquad b = \begin{pmatrix} 5 \\\ 7 \end{pmatrix},
$$

using $x = A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

---

## Solution

We are given the linear system $Ax = b$ with coefficient matrix $A$ and right-hand side vector $b$[span_1](start_span)[span_1](end_span):

$$
A = \begin{pmatrix} 2 & 1 \\\ 1 & 3 \end{pmatrix}, \qquad b = \begin{pmatrix} 5 \\\ 7 \end{pmatrix}
$$

---

### 1. Find the Inverse Matrix $A^{-1}$

First, we compute the determinant of $A$:

$$
\det(A) = (2)(3) - (1)(1) = 6 - 1 = 5
$$

Since $\det(A) = 5 \neq 0$, $A^{-1}$ exists. Applying the $2 \times 2$ inverse formula:

$$
A^{-1} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\\ -1 & 2 \end{pmatrix} = \begin{pmatrix} \frac{3}{5} & -\frac{1}{5} \\\ -\frac{1}{5} & \frac{2}{5} \end{pmatrix}
$$

---

### 2. Solve for $x$ Using $x = A^{-1}b$

Multiplying $A^{-1}$ by the vector $b$[span_2](start_span)[span_2](end_span):

$$
x = A^{-1}b = \frac{1}{5} \begin{pmatrix} 3 & -1 \\\ -1 & 2 \end{pmatrix} \begin{pmatrix} 5 \\\ 7 \end{pmatrix}
$$

Evaluating each component:

* First component ($x_1$): $\frac{1}{5} \big((3)(5) + (-1)(7)\big) = \frac{1}{5}(15 - 7) = \frac{8}{5}$
* Second component ($x_2$): $\frac{1}{5} \big((-1)(5) + (2)(7)\big) = \frac{1}{5}(-5 + 14) = \frac{9}{5}$

Thus, the solution vector is:

$$
x = \begin{pmatrix} \frac{8}{5} \\\ \frac{9}{5} \end{pmatrix}
$$

---

### 3. Check the Result by Substitution

Substituting $x$ back into the original equation $Ax = b$[span_3](start_span)[span_3](end_span):

$$
Ax = \begin{pmatrix} 2 & 1 \\\ 1 & 3 \end{pmatrix} \begin{pmatrix} \frac{8}{5} \\\ \frac{9}{5} \end{pmatrix} = \begin{pmatrix} 2\left(\frac{8}{5}\right) + 1\left(\frac{9}{5}\right) \\\ 1\left(\frac{8}{5}\right) + 3\left(\frac{9}{5}\right) \end{pmatrix} = \begin{pmatrix} \frac{16}{5} + \frac{9}{5} \\\ \frac{8}{5} + \frac{27}{5} \end{pmatrix} = \begin{pmatrix} \frac{25}{5} \\\ \frac{35}{5} \end{pmatrix} = \begin{pmatrix} 5 \\\ 7 \end{pmatrix} = b
$$

Since $Ax = b$ holds, the solution is verified[span_4](start_span)[span_4](end_span).

---

### Conclusion

* The inverse matrix is:

$$
A^{-1} = \begin{pmatrix} \frac{3}{5} & -\frac{1}{5} \\\ -\frac{1}{5} & \frac{2}{5} \end{pmatrix}
$$

* The unique solution to the system $Ax = b$ is:

$$
x = \begin{pmatrix} \frac{8}{5} \\\ \frac{9}{5} \end{pmatrix}
$$
