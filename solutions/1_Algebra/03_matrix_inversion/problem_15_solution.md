# Exercise 15. Two Methods for Solving the Same System

## Question

For

$$
A = \begin{pmatrix} 2 & 1 \\\ 1 & 3 \end{pmatrix}, \qquad b = \begin{pmatrix} 7 \\\ 8 \end{pmatrix}
$$

solve $Ax = b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

---

## Solution

We want to solve the $2 \times 2$ linear system $Ax = b$, where:

$$
A = \begin{pmatrix} 2 & 1 \\\ 1 & 3 \end{pmatrix}, \qquad b = \begin{pmatrix} 7 \\\ 8 \end{pmatrix}, \qquad x = \begin{pmatrix} x_1 \\\ x_2 \end{pmatrix}
$$

---

### 1. Method 1: Solving via $x = A^{-1}b$

**Step 1: Compute the determinant of $A$**

$$
\det(A) = (2)(3) - (1)(1) = 6 - 1 = 5
$$

Since $\det(A) = 5 \neq 0$, $A$ is invertible.

**Step 2: Find $A^{-1}$ using the $2 \times 2$ inverse formula**

$$
A^{-1} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\\ -1 & 2 \end{pmatrix} = \begin{pmatrix} \frac{3}{5} & -\frac{1}{5} \\\ -\frac{1}{5} & \frac{2}{5} \end{pmatrix}
$$

**Step 3: Multiply $A^{-1}$ by $b$ to obtain $x$**

$$
x = A^{-1}b = \frac{1}{5} \begin{pmatrix} 3 & -1 \\\ -1 & 2 \end{pmatrix} \begin{pmatrix} 7 \\\ 8 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} (3)(7) + (-1)(8) \\\ (-1)(7) + (2)(8) \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 21 - 8 \\\ -7 + 16 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 13 \\\ 9 \end{pmatrix} = \begin{pmatrix} \frac{13}{5} \\\ \frac{9}{5} \end{pmatrix}
$$

---

### 2. Method 2: Solving via Gaussian Elimination

We form the augmented matrix $[A \mid b]$:

$$
\left( \begin{array}{cc|c} 2 & 1 & 7 \\\ 1 & 3 & 8 \end{array} \right)
$$

**Step 1: Swap Row 1 and Row 2 ($R_1 \leftrightarrow R_2$) to get a leading $1$**

$$
\left( \begin{array}{cc|c} 1 & 3 & 8 \\\ 2 & 1 & 7 \end{array} \right)
$$

**Step 2: Eliminate the entry below the pivot ($R_2 \leftarrow R_2 - 2R_1$)**

$$
\left( \begin{array}{cc|c} 1 & 3 & 8 \\\ 0 & -5 & -9 \end{array} \right)
$$

**Step 3: Back-substitution**

From the second row:

$$
-5x_2 = -9 \quad \Longrightarrow \quad x_2 = \frac{9}{5}
$$

Substituting $x_2 = \frac{9}{5}$ into the first row ($x_1 + 3x_2 = 8$):

$$
x_1 + 3\left(\frac{9}{5}\right) = 8 \quad \Longrightarrow \quad x_1 = 8 - \frac{27}{5} = \frac{40 - 27}{5} = \frac{13}{5}
$$

Thus, the solution vector is:

$$
x = \begin{pmatrix} \frac{13}{5} \\\ \frac{9}{5} \end{pmatrix}
$$

---

### 3. Comparison of Both Methods

* **Solution agreement:** Both methods yield the exact same unique solution:

$$
x = \begin{pmatrix} \frac{13}{5} \\\ \frac{9}{5} \end{pmatrix}
$$

* **Number of essential steps:**
  * **Method 1 ($A^{-1}b$):** Requires **3 essential steps** (computing $\det(A)$, forming $A^{-1}$, and performing a matrix–vector multiplication $A^{-1}b$).
  * **Method 2 (Gaussian elimination):** Requires **3 essential steps** (one row swap, one row elimination operation, and back-substitution).
* **Which method was simpler in this example:**
  * **Gaussian elimination** was slightly simpler and cleaner for solving a single right-hand side $b$, because all row operations used small integers ($1, 2, 3, -5, -9$) and fractions appeared only at the final back-substitution step.
  * By contrast, computing $A^{-1}$ introduces fractions across all four matrix entries (or requires factoring out $\frac{1}{5}$) and performs extra arithmetic that is unnecessary unless we need to solve $Ax = b$ repeatedly for multiple different vectors $b$.

---

### Conclusion

* Both $A^{-1}b$ and Gaussian elimination yield:

$$
x = \begin{pmatrix} \frac{13}{5} \\\ \frac{9}{5} \end{pmatrix}
$$

* Both take 3 essential steps, but **Gaussian elimination** is simpler for a single system because it avoids constructing the full inverse matrix and delays fraction arithmetic until the very end.
