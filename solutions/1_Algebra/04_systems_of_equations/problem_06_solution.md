# Exercise 6. A System with a Parameter — Which Cases Actually Occur?

## Question

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x + y = 2, \\\
ax + ay = 4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

---

## Solution

We write the augmented matrix of the system:

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ a & a & 4 \end{array} \right)
$$

---

### 1. Row Reduction Depending on $a$

Perform the elementary row operation $R_2 \leftarrow R_2 - aR_1$ to eliminate the entry below the pivot:

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 0 & 0 & 4 - 2a \end{array} \right)
$$

The second row corresponds to the equation:

$$
0x + 0y = 4 - 2a \quad \Longleftrightarrow \quad 0 = 4 - 2a
$$

---

### 2. Case-by-Case Analysis of the Three Possibilities

1. **Infinitely Many Solutions ($a = 2$):**
   * Setting the right-hand side of Row 2 equal to zero gives $4 - 2a = 0 \implies a = 2$.
   * When $a = 2$, the augmented matrix becomes:

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 0 & 0 & 0 \end{array} \right)
$$

   * The second equation ($2x + 2y = 4$) is simply twice the first equation ($x + y = 2$). Letting $y = t \in \mathbb{R}$ gives infinitely many solutions: $(x, y) = (2 - t, \, t)$.

2. **No Solution ($a \neq 2$):**
   * Whenever $a \neq 2$, we have $4 - 2a \neq 0$.
   * Row 2 becomes $0 = 4 - 2a \neq 0$, which is a contradiction (for example, if $a = 0$, $0 = 4$; if $a = 1$, $x + y = 2$ and $x + y = 4$ represent two parallel lines).
   * Therefore, the system is inconsistent and has **no solution** for all $a \neq 2$.

3. **Exactly One Solution (Never Occurs):**
   * **Why it cannot occur:** For any $a \in \mathbb{R}$, the coefficient matrix is:

$$
A = \begin{pmatrix} 1 & 1 \\\ a & a \end{pmatrix}
$$

   * Its second row $(a, a)$ is always a scalar multiple of its first row $(1, 1)$, so $\det(A) = 1 \cdot a - 1 \cdot a = 0$ for every value of $a$.
   * Because the rank of the coefficient matrix can never be $2$ (there is always a free variable whenever the system is consistent), the lines $x + y = 2$ and $ax + ay = 4$ can never intersect at a single unique point.

---

### Conclusion

* **Infinitely many solutions:** Occurs only when **$a = 2$**.
* **No solution:** Occurs for all **$a \neq 2$**.
* **Exactly one solution:** **Never occurs** for any $a \in \mathbb{R}$, because the coefficient rows $(1, 1)$ and $(a, a)$ are always linearly dependent ($\det(A) = 0$).
