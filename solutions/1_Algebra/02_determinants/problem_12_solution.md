# Exercise 12. A Parameter Revealed by a Row Operation

## Question

For

$$
A(t) = \begin{pmatrix} 1 & 2 & 3 \\\ 2 & 4 & t \\\ 0 & 1 & 1 \end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2 \leftarrow R_2 - 2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

---

## Solution

A square matrix is not invertible (singular) if and only if its determinant is zero:

$$
\det(A(t)) = 0
$$

We simplify the matrix using the requested row operation before evaluating the determinant.

---

### Step 1: Perform the Row Operation $R_2 \leftarrow R_2 - 2R_1$

* **Effect on determinant:**  
  Adding a scalar multiple of one row to another row does not change the determinant ($\det \text{ remains unchanged}$).

* **Calculation for row 2:**

$$
(2, 4, t) - 2(1, 2, 3) = (2 - 2, \, 4 - 4, \, t - 6) = (0, 0, t - 6)
$$

The matrix becomes:

$$
\tilde{A}(t) = \begin{pmatrix} 1 & 2 & 3 \\\ 0 & 0 & t - 6 \\\ 0 & 1 & 1 \end{pmatrix}
$$

Since the row operation preserves the determinant:

$$
\det(A(t)) = \det(\tilde{A}(t))
$$

---

### Step 2: Compute the Determinant Using the Resulting Structure

We compute $\det(\tilde{A}(t))$ by expanding along the second row, which contains two zero entries:

$$
\det(\tilde{A}(t)) = 0 \cdot C_{21} + 0 \cdot C_{22} + (t - 6) \cdot C_{23}
$$

The cofactor $C_{23}$ is:

$$
C_{23} = (-1)^{2+3} \det \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix} = -1 \cdot ((1)(1) - (2)(0)) = -1
$$

Therefore:

$$
\det(A(t)) = (t - 6) \cdot (-1) = -(t - 6) = 6 - t
$$

---

### Step 3: Find the Value of $t$ for Noninvertibility

To find the value of $t$ where the matrix is not invertible, set the determinant to zero:

$$
6 - t = 0 \implies t = 6
$$

Thus, the matrix $A(t)$ is not invertible when $t = 6$.

---

### Step 4: Special Relationship Between the Rows When $t = 6$

When $t = 6$, substituting into the original matrix gives:

$$
A(6) = \begin{pmatrix} 1 & 2 & 3 \\\ 2 & 4 & 6 \\\ 0 & 1 & 1 \end{pmatrix}
$$

Comparing row 1 ($\mathbf{r}_1$) and row 2 ($\mathbf{r}_2$):

$$
\mathbf{r}_2 = (2, 4, 6) = 2 \cdot (1, 2, 3) = 2 \mathbf{r}_1
$$

* **Linear Dependence:**  
  Row 2 is an exact scalar multiple of row 1 ($\mathbf{r}_2 = 2\mathbf{r}_1$), meaning the rows are linearly dependent ($2\mathbf{r}_1 - \mathbf{r}_2 = \mathbf{0}$).
* **Consequence of the Row Operation:**  
  Because row 2 is twice row 1, the row operation $R_2 \leftarrow R_2 - 2R_1$ turns the entire second row into a **row of zeros**:

$$
(0, 0, 6 - 6) = (0, 0, 0)
$$

A matrix containing an all-zero row after row reduction cannot have full rank ($\text{rank}(A) \le 2 < 3$) and must have determinant equal to $0$, confirming that it cannot be inverted.

---

### Conclusion

* **Row Operation Result:**

$$
\det(A(t)) = \det \begin{pmatrix} 1 & 2 & 3 \\\ 0 & 0 & t - 6 \\\ 0 & 1 & 1 \end{pmatrix} = 6 - t
$$

* **Value for Noninvertibility:**

$$
t = 6
$$

* **Special Row Behavior:** At $t = 6$, row 2 is an exact scalar multiple of row 1 ($\mathbf{r}_2 = 2\mathbf{r}_1$). This linear dependence causes row 2 to become completely zero under the operation $R_2 \leftarrow R_2 - 2R_1$, proving that $\det(A(6)) = 0$ and the matrix is singular.
