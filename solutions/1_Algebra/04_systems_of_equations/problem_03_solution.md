# Exercise 3. Inconsistent System

## Question

Solve or show that the system is inconsistent:

$$
\begin{cases}
x + 2y = 3, \\\
2x + 4y = 7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

---

## Solution

We write the augmented matrix for the $2 \times 2$ linear system:

$$
\left( \begin{array}{cc|c} 1 & 2 & 3 \\\ 2 & 4 & 7 \end{array} \right)
$$

---

### 1. Apply Gaussian Elimination

Perform the elementary row operation $R_2 \leftarrow R_2 - 2R_1$ to eliminate the $x$-entry below the first pivot:

$$
\left( \begin{array}{cc|c} 1 & 2 & 3 \\\ 0 & 0 & 1 \end{array} \right)
$$

---

### 2. How the Contradiction Appears in the Matrix

In the reduced augmented matrix, the second row has all zeros on the left-hand side of the vertical bar and a non-zero constant on the right-hand side:

$$
\left( \begin{array}{cc|c} 0 & 0 & 1 \end{array} \right)
$$

This row has the inconsistent form $(0 \;\; 0 \mid c)$ with $c = 1 \neq 0$, which proves immediately that the system is **inconsistent** and has **no solution**.

---

### 3. Interpretation in Terms of Equations

* Translating the second row back into an algebraic equation gives:

$$
0x + 0y = 1 \quad \Longleftrightarrow \quad 0 = 1
$$

which is a mathematical contradiction that cannot be satisfied by any pair of real numbers $(x, y)$.
* Comparing the original equations directly, multiplying the first equation ($x + 2y = 3$) by $2$ requires $2x + 4y = 6$, which directly contradicts the second equation $2x + 4y = 7$ (geometrically, these represent two distinct parallel lines that never intersect).

---

### Conclusion

* **Consistency:** The system is **inconsistent** and has **no solution**.
* **Matrix contradiction:** Elimination produces the row $(0 \;\; 0 \mid 1)$, corresponding to the impossible equation $0 = 1$.
