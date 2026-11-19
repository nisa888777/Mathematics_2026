# Exercise 7. Choosing a Method Deliberately

## Question

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x - y = 3, \\\
4y = 8;
\end{cases}
$$

2. three systems $Ax = b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3 \times 3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

---

## Solution

### 1. Case 1: One System with a Triangular Coefficient Matrix

* **Chosen Method:** Direct **back-substitution** (no elimination or matrix inversion needed).
* **Justification:** There is only $1$ right-hand side, and the coefficient matrix $A = \begin{pmatrix} 2 & -1 \\\ 0 & 4 \end{pmatrix}$ is already in upper-triangular form. Row reduction or computing $A^{-1}$ would perform unnecessary work since the last variable $y$ is already isolated.
* **Complete Execution:**
  1. From the second equation ($4y = 8$):

$$
y = \frac{8}{4} = 2
$$

  2. Substitute $y = 2$ into the first equation ($2x - y = 3$):

$$
2x - 2 = 3 \quad \Longrightarrow \quad 2x = 5 \quad \Longrightarrow \quad x = \frac{5}{2}
$$

Thus, the unique solution is $(x, y) = \left(\frac{5}{2}, 2\right)$.

---

### 2. Case 2: Three Systems $Ax = b_i$ with Known $A^{-1}$

* **Chosen Method:** Direct matrix–vector multiplication **$x_i = A^{-1}b_i$** for each $i = 1, 2, 3$ (or multiplying $A^{-1}[b_1 \;\; b_2 \;\; b_3]$ in one block).
* **Justification & Plan:**
  * **Reusable part:** Because $A^{-1}$ is **already known**, the most expensive step (inverting $A$) is completely avoided and $A^{-1}$ is reused directly across all $3$ right-hand sides $b_1, b_2, b_3$.
  * **Unnecessary part:** Running Gaussian elimination three separate times from scratch would repeatedly apply the same row operations to $A$. Simply computing $x_1 = A^{-1}b_1$, $x_2 = A^{-1}b_2$, and $x_3 = A^{-1}b_3$ solves all three systems with minimal arithmetic.

---

### 3. Case 3: One $3 \times 3$ System Without Known $A^{-1}$

* **Chosen Method:** **Gaussian elimination** with back-substitution on the augmented matrix $[A \mid b]$.
* **Justification & Plan:**
  * **Plan:** Form the $3 \times 4$ augmented matrix $[A \mid b]$, use elementary row operations to reduce $A$ to upper-triangular (row echelon) form, and find the single solution vector $x$ via back-substitution.
  * **Unnecessary part:** Computing $A^{-1}$ via Gauss–Jordan elimination on $[A \mid I_3]$ requires reducing a wider $3 \times 6$ matrix all the way to reduced row echelon form $[I_3 \mid A^{-1}]$, which computes all $9$ entries of $A^{-1}$ even though there is only **$1$ right-hand side** and we never reuse $A$ again.

---

### Conclusion

* **Case 1:** Use **back-substitution** directly because the matrix is already triangular; the solution is $(x, y) = \left(\frac{5}{2}, 2\right)$.
* **Case 2:** Use **$x_i = A^{-1}b_i$** because $A^{-1}$ is already available and can be reused across all $3$ right-hand sides without repeating elimination.
* **Case 3:** Use **Gaussian elimination** on $[A \mid b]$ because finding $A^{-1}$ does unnecessary extra work for a single $3 \times 3$ right-hand side.
