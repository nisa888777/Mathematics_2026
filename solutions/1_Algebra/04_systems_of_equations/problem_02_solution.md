# Exercise 2. Gaussian Elimination — One Solution

## Question

Solve using Gaussian elimination:

$$
\begin{cases}
x + y + z = 6, \\\
2x - y + z = 3, \\\
x + 2y - z = 2.
\end{cases}
$$

After solving, substitute the result into all equations and check consistency.

---

## Solution

We form the augmented matrix for the $3 \times 3$ linear system:

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 6 \\\ 2 & -1 & 1 & 3 \\\ 1 & 2 & -1 & 2 \end{array} \right)
$$

---

### 1. Forward Elimination (Reduce to Row Echelon Form)

**Step 1: Eliminate $x$ from Row 2 ($R_2 \leftarrow R_2 - 2R_1$) and Row 3 ($R_3 \leftarrow R_3 - R_1$)**

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 6 \\\ 0 & -3 & -1 & -9 \\\ 0 & 1 & -2 & -4 \end{array} \right)
$$

**Step 2: Swap Row 2 and Row 3 ($R_2 \leftrightarrow R_3$) to get a leading $1$ in the second pivot**

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 6 \\\ 0 & 1 & -2 & -4 \\\ 0 & -3 & -1 & -9 \end{array} \right)
$$

**Step 3: Eliminate $y$ from Row 3 ($R_3 \leftarrow R_3 + 3R_2$)**

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 6 \\\ 0 & 1 & -2 & -4 \\\ 0 & 0 & -7 & -21 \end{array} \right)
$$

---

### 2. Back-Substitution

From the triangular system represented by the row echelon form:

1. **From Row 3 ($-7z = -21$):**

$$
z = \frac{-21}{-7} = 3
$$

2. **From Row 2 ($y - 2z = -4$):**

$$
y - 2(3) = -4 \quad \Longrightarrow \quad y - 6 = -4 \quad \Longrightarrow \quad y = 2
$$

3. **From Row 1 ($x + y + z = 6$):**

$$
x + 2 + 3 = 6 \quad \Longrightarrow \quad x + 5 = 6 \quad \Longrightarrow \quad x = 1
$$

Thus, the unique solution is $(x, y, z) = (1, 2, 3)$.

---

### 3. Substitute the Result into All Equations to Check Consistency

Substituting $(x, y, z) = (1, 2, 3)$ into each original equation:

1. **Equation 1 ($x + y + z = 6$):**

$$
1 + 2 + 3 = 6 \quad \checkmark
$$

2. **Equation 2 ($2x - y + z = 3$):**

$$
2(1) - 2 + 3 = 2 - 2 + 3 = 3 \quad \checkmark
$$

3. **Equation 3 ($x + 2y - z = 2$):**

$$
1 + 2(2) - 3 = 1 + 4 - 3 = 2 \quad \checkmark
$$

All three equations are satisfied identically, confirming that the system is consistent and $(1, 2, 3)$ is the exact solution.

---

### Conclusion

* **Unique solution:** $(x, y, z) = (1, 2, 3)$.
* **Consistency check:** Substituting $x = 1$, $y = 2$, and $z = 3$ satisfies all three equations ($6 = 6$, $3 = 3$, and $2 = 2$).
