# Exercise 3. When Does the Inverse Not Exist?

## Question

For

$$
A = \begin{pmatrix} 2 & 4 \\\ 1 & 2 \end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

---

## Solution

We are given the $2 \times 2$ matrix:

$$
A = \begin{pmatrix} 2 & 4 \\\ 1 & 2 \end{pmatrix}
$$

---

### 1. Explanation Using the Determinant

A square matrix $A$ is invertible if and only if its determinant is non-zero ($\det(A) \neq 0$). Computing the determinant of $A$:

$$
\det(A) = (2)(2) - (4)(1) = 4 - 4 = 0
$$

Because $\det(A) = 0$, the $2 \times 2$ inverse formula

$$
A^{-1} = \frac{1}{\det(A)} \begin{pmatrix} d & -b \\\ -c & a \end{pmatrix}
$$

would require division by zero ($\frac{1}{0}$), which is undefined. Thus, $A^{-1}$ does not exist.

---

### 2. Explanation Using Linear Dependence Between the Rows

Let the rows of $A$ be $\mathbf{r}_1 = (2, 4)$ and $\mathbf{r}_2 = (1, 2)$. Notice that the first row is a scalar multiple of the second row:

$$
\mathbf{r}_1 = 2\mathbf{r}_2 \qquad \text{(equivalently, } \mathbf{r}_1 - 2\mathbf{r}_2 = \mathbf{0}\text{)}
$$

Because the rows are linearly dependent:

* During Gauss–Jordan elimination ($R_1 \leftarrow R_1 - 2R_2$), the first row becomes a row of zeros:

$$
\begin{pmatrix} 2 & 4 \\\ 1 & 2 \end{pmatrix} \longrightarrow \begin{pmatrix} 0 & 0 \\\ 1 & 2 \end{pmatrix}
$$

* Since a matrix with a zero row cannot be reduced to the $2 \times 2$ identity matrix $I$, no inverse matrix $A^{-1}$ can exist.

---

### Conclusion

* **Determinant test:** $\det(A) = 0$, so $A$ is singular.
* **Row dependence:** Row $1$ is twice Row $2$ ($\mathbf{r}_1 = 2\mathbf{r}_2$), meaning $A$ cannot be row-reduced to the identity matrix $I$. Therefore, **$A^{-1}$ does not exist**.
