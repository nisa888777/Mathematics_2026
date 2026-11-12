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

A square matrix is invertible if and only if it is non-singular (has a non-zero determinant and linearly independent rows). Below are two equivalent explanations for why $A^{-1}$ does not exist.

---

### 1. Explanation Using the Determinant

For a $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\\ c & d \end{pmatrix}$, the determinant is given by $\det(A) = ad - bc$. Substituting the entries of $A$:

$$
\det(A) = (2)(2) - (4)(1) = 4 - 4 = 0
$$

Since the inverse formula requires dividing by the determinant ($\frac{1}{\det(A)}$) and division by zero is undefined, a matrix with $\det(A) = 0$ is singular and cannot have an inverse.

---

### 2. Explanation Using Linear Dependence Between the Rows

Let $\mathbf{r}_1$ and $\mathbf{r}_2$ denote the first and second rows of $A$:

$$
\mathbf{r}_1 = \begin{pmatrix} 2 & 4 \end{pmatrix}, \qquad \mathbf{r}_2 = \begin{pmatrix} 1 & 2 \end{pmatrix}
$$

Notice that the first row is an exact scalar multiple of the second row:

$$
\mathbf{r}_1 = 2\mathbf{r}_2 \quad \Longleftrightarrow \quad \mathbf{r}_1 - 2\mathbf{r}_2 = \begin{pmatrix} 0 & 0 \end{pmatrix}
$$

Because one row can be expressed as a linear combination of the other, the rows of $A$ are **linearly dependent**. Applying the elementary row operation $R_1 \leftarrow R_1 - 2R_2$ produces a zero row:

$$
\begin{pmatrix} 2 & 4 \\\ 1 & 2 \end{pmatrix} \xrightarrow{R_1 \leftarrow R_1 - 2R_2} \begin{pmatrix} 0 & 0 \\\ 1 & 2 \end{pmatrix}
$$

Since $A$ cannot be reduced to the $2 \times 2$ identity matrix $I$, it is non-invertible.

---

### Conclusion

* **Determinant criterion:** $\det(A) = 0$, so $A$ is singular.
* **Row dependence criterion:** $\mathbf{r}_1 = 2\mathbf{r}_2$, meaning the rows are linearly dependent and $A$ cannot be row-reduced to $I$.
* Therefore, **$A^{-1}$ does not exist**.
