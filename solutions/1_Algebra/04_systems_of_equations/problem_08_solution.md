# Exercise 8. Two Systems with the Same Coefficient Matrix

## Question

Solve by elimination the two systems

$$
\begin{cases}
2x + y = 5, \\\
x - y = 1,
\end{cases}
$$

$$
\begin{cases}
2x + y = 1, \\\
x - y = 4.
\end{cases}
$$

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

---

## Solution

Both systems share the exact same $2 \times 2$ coefficient matrix:

$$
A = \begin{pmatrix} 2 & 1 \\\ 1 & -1 \end{pmatrix}
$$

---

### 1. Solve the First System

We write the augmented matrix for the first system:

$$
\left( \begin{array}{cc|c} 2 & 1 & 5 \\\ 1 & -1 & 1 \end{array} \right)
$$

* **Step 1:** Swap Row 1 and Row 2 ($R_1 \leftrightarrow R_2$) to obtain a leading $1$ in the first pivot:

$$
\left( \begin{array}{cc|c} 1 & -1 & 1 \\\ 2 & 1 & 5 \end{array} \right)
$$

* **Step 2:** Eliminate $x$ from Row 2 ($R_2 \leftarrow R_2 - 2R_1$):

$$
\left( \begin{array}{cc|c} 1 & -1 & 1 \\\ 0 & 3 & 3 \end{array} \right)
$$

* **Step 3:** Back-substitution:

$$
3y = 3 \implies y = 1, \qquad x - 1 = 1 \implies x = 2
$$

Thus, the solution to the first system is $(x, y) = (2, 1)$.

---

### 2. Solve the Second System

We write the augmented matrix for the second system:

$$
\left( \begin{array}{cc|c} 2 & 1 & 1 \\\ 1 & -1 & 4 \end{array} \right)
$$

* **Step 1:** Swap Row 1 and Row 2 ($R_1 \leftrightarrow R_2$):

$$
\left( \begin{array}{cc|c} 1 & -1 & 4 \\\ 2 & 1 & 1 \end{array} \right)
$$

* **Step 2:** Eliminate $x$ from Row 2 ($R_2 \leftarrow R_2 - 2R_1$):

$$
\left( \begin{array}{cc|c} 1 & -1 & 4 \\\ 0 & 3 & -7 \end{array} \right)
$$

* **Step 3:** Back-substitution:

$$
3y = -7 \implies y = -\frac{7}{3}, \qquad x - \left(-\frac{7}{3}\right) = 4 \implies x = 4 - \frac{7}{3} = \frac{5}{3}
$$

Thus, the solution to the second system is $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$.

---

### 3. Comparison of Elimination Steps and Explanation

* **What is identical in both cases:**
  1. The **sequence of elementary row operations** ($R_1 \leftrightarrow R_2$, followed by $R_2 \leftarrow R_2 - 2R_1$) is completely identical.
  2. The **left-hand side coefficient entries** at every intermediate stage—and the resulting upper-triangular coefficient matrix—are identical in both systems:

$$
\begin{pmatrix} 1 & -1 \\\ 0 & 3 \end{pmatrix}
$$

* **What differs:** Only the numerical values in the **right-hand side column** change, because the initial right-hand side vectors $(5, 1)^T$ and $(1, 4)^T$ are different.
* **Why:** Elementary row operations used to introduce zeros below the pivots depend solely on the entries of the **coefficient matrix $A$**. The right-hand side vector $b$ does not determine which row operations or multipliers are chosen; it simply undergoes the same linear transformations alongside $A$.

---

### Conclusion

* **First system solution:** $(x, y) = (2, 1)$.
* **Second system solution:** $(x, y) = \left(\frac{5}{3}, -\frac{7}{3}\right)$.
* **Comparison:** Both systems undergo the exact same row operations ($R_1 \leftrightarrow R_2$ and $R_2 \leftarrow R_2 - 2R_1$) and produce the same upper-triangular coefficient matrix, because the elimination process is governed entirely by the shared coefficient matrix $A$, independently of the right-hand side vector.
