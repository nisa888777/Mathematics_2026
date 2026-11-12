# Exercise 9. Matrix Equation

## Question

Given

$$
A = \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 3 & 1 \\\ 2 & 4 \end{pmatrix}.
$$

Solve the equation $AX = B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

---

## Solution

We are given the $2 \times 2$ matrices:

$$
A = \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 3 & 1 \\\ 2 & 4 \end{pmatrix}
$$

---

### 1. Decide on Which Side $A^{-1}$ Must Be Used

In the matrix equation $AX = B$, the matrix $A$ multiplies $X$ from the **left**. Since matrix multiplication is not commutative in general ($A^{-1}B \neq BA^{-1}$), we must multiply both sides of the equation by $A^{-1}$ on the **left** to isolate $X$:

$$
A^{-1}(AX) = A^{-1}B
$$

Using the associative property of matrix multiplication:

$$
(A^{-1}A)X = A^{-1}B \quad \Longrightarrow \quad IX = A^{-1}B \quad \Longrightarrow \quad X = A^{-1}B
$$

Note: Multiplying on the right would yield $AXA^{-1} = BA^{-1}$, which does not simplify to isolate $X$.

---

### 2. Compute $A^{-1}$

First, we compute the determinant of $A$:

$$
\det(A) = (1)(1) - (2)(0) = 1
$$

Since $\det(A) = 1 \neq 0$, $A^{-1}$ exists. Applying the $2 \times 2$ inverse formula:

$$
A^{-1} = \frac{1}{1} \begin{pmatrix} 1 & -2 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -2 \\\ 0 & 1 \end{pmatrix}
$$

---

### 3. Solve for $X$

Substituting $A^{-1}$ and $B$ into $X = A^{-1}B$:

$$
X = \begin{pmatrix} 1 & -2 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 3 & 1 \\\ 2 & 4 \end{pmatrix} = \begin{pmatrix} (1)(3) + (-2)(2) & (1)(1) + (-2)(4) \\\ (0)(3) + (1)(2) & (0)(1) + (1)(4) \end{pmatrix} = \begin{pmatrix} 3 - 4 & 1 - 8 \\\ 0 + 2 & 0 + 4 \end{pmatrix} = \begin{pmatrix} -1 & -7 \\\ 2 & 4 \end{pmatrix}
$$

---

### 4. Check the Result by Computing $AX$

We substitute $X$ back into $AX$ to verify that it equals $B$:

$$
AX = \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} -1 & -7 \\\ 2 & 4 \end{pmatrix} = \begin{pmatrix} (1)(-1) + (2)(2) & (1)(-7) + (2)(4) \\\ (0)(-1) + (1)(2) & (0)(-7) + (1)(4) \end{pmatrix} = \begin{pmatrix} -1 + 4 & -7 + 8 \\\ 0 + 2 & 0 + 4 \end{pmatrix} = \begin{pmatrix} 3 & 1 \\\ 2 & 4 \end{pmatrix} = B
$$

Since $AX = B$, the solution matrix $X$ is verified.

---

### Conclusion

* Because $A$ appears on the left of $X$ in $AX = B$, $A^{-1}$ must be multiplied on the **left** ($X = A^{-1}B$).
* The solution matrix is:

$$
X = \begin{pmatrix} -1 & -7 \\\ 2 & 4 \end{pmatrix}
$$
