# Exercise 14. A System of Equations and the Determinant

## Question

Consider the system $Ax = b$, where

$$
A = \begin{pmatrix} 1 & 2 \\\ k & 4 \end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

---

## Solution

We are analyzing the linear system $Ax = b$, where the coefficient matrix is:

$$
A = \begin{pmatrix} 1 & 2 \\\ k & 4 \end{pmatrix}
$$

---

### 1. Condition for a Unique Solution for Every $b$

A square linear system $Ax = b$ has **exactly one unique solution** for every right-hand side vector $b \in \mathbb{R}^2$ if and only if the coefficient matrix $A$ is invertible, which is equivalent to $\det(A) \neq 0$.

Computing the determinant of $A$:

$$
\det(A) = (1)(4) - (2)(k) = 4 - 2k
$$

Setting $\det(A) \neq 0$:

$$
4 - 2k \neq 0 \implies 2k \neq 4 \implies k \neq 2
$$

Thus, for all $k \neq 2$, the matrix $A$ is invertible and the system $Ax = b$ has a unique solution $x = A^{-1}b$ for every $b$.

---

### 2. Analysis of the Remaining Value ($k = 2$)

When $k = 2$, the determinant vanishes ($\det(A) = 0$) and the matrix becomes:

$$
A = \begin{pmatrix} 1 & 2 \\\ 2 & 4 \end{pmatrix}
$$

Writing out the system $Ax = b$ with unknown vector $x = (x_1, x_2)^T$ and right-hand side $b = (b_1, b_2)^T$ gives:

$$
\begin{cases}
x_1 + 2x_2 = b_1 \\
2x_1 + 4x_2 = b_2
\end{cases}
$$

Notice that the left-hand side of the second equation is exact twice the first equation ($2(x_1 + 2x_2) = 2x_1 + 4x_2$). Therefore, the system is consistent if and only if $b_2 = 2b_1$.

* **Example for Infinitely Many Solutions ($b_2 = 2b_1$):**  
  Choose

$$
b = \begin{pmatrix} 3 \\\ 6 \end{pmatrix}
$$

  Then the second equation $2x_1 + 4x_2 = 6$ is simply $2$ times the first equation $x_1 + 2x_2 = 3$. They represent the same line, so any pair $(x_1, x_2) = (3 - 2t, \, t)$ with $t \in \mathbb{R}$ is a solution, yielding **infinitely many solutions**.

* **Example for No Solution ($b_2 \neq 2b_1$):**  
  Choose

$$
b = \begin{pmatrix} 3 \\\ 5 \end{pmatrix}
$$

  Subtracting twice the first equation from the second gives $0 = 5 - 2(3) = -1$, a contradiction. The two equations represent parallel distinct lines, so the system is inconsistent and has **no solution**.

---

### Conclusion

* **Unique solution for every $b$:** Occurs for all **$k \neq 2$**.
* **Infinitely many solutions (at $k = 2$):** Example

$$
b = \begin{pmatrix} 3 \\\ 6 \end{pmatrix}
$$

* **No solution (at $k = 2$):** Example

$$
b = \begin{pmatrix} 3 \\\ 5 \end{pmatrix}
$$
