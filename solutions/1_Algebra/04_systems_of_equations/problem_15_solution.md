# Exercise 15. Classifying Three Systems

## Question

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x + y = 2, \\\
x - y = 0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x + y = 2, \\\
2x + 2y = 4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x + y = 2, \\\
2x + 2y = 5.
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

---

## Solution

We apply a single elementary row operation to each $2 \times 3$ augmented matrix to eliminate $x$ from the second row and reveal its echelon structure.

---

### 1. System 1

Form the augmented matrix and apply $R_2 \leftarrow R_2 - R_1$:

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 1 & -1 & 0 \end{array} \right) \xrightarrow{R_2 \leftarrow R_2 - R_1} \left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 0 & -2 & -2 \end{array} \right)
$$

* **Classification:** **One solution** (unique solution).
* **Justification:** Both variable columns (Column 1 and Column 2) contain non-zero pivots ($1$ and $-2$), so there are $r = 2$ pivots for $n = 2$ unknowns and $n - r = 0$ free variables. Back-substitution uniquely determines $y = 1$ and $x = 1$, giving the unique solution $(x, y) = (1, 1)$.

---

### 2. System 2

Form the augmented matrix and apply $R_2 \leftarrow R_2 - 2R_1$:

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 2 & 2 & 4 \end{array} \right) \xrightarrow{R_2 \leftarrow R_2 - 2R_1} \left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 0 & 0 & 0 \end{array} \right)
$$

* **Classification:** **Infinitely many solutions**.
* **Justification:** The second row reduces completely to $(0 \;\; 0 \mid 0)$ ($0x + 0y = 0$), which is always satisfied and introduces no contradiction. There is only $r = 1$ pivot (in Column 1) for $n = 2$ unknowns, leaving $n - r = 1$ free variable ($y = t \in \mathbb{R}$, with $x = 2 - t$). Because $t$ can take infinitely many real values, the system has infinitely many solutions.

---

### 3. System 3

Form the augmented matrix and apply $R_2 \leftarrow R_2 - 2R_1$:

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 2 & 2 & 5 \end{array} \right) \xrightarrow{R_2 \leftarrow R_2 - 2R_1} \left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 0 & 0 & 1 \end{array} \right)
$$

* **Classification:** **No solution** (inconsistent system).
* **Justification:** The second row reduces to $(0 \;\; 0 \mid 1)$, which represents the equation $0x + 0y = 1$ ($0 = 1$). Since $0 = 1$ is a contradiction that cannot be satisfied by any values of $x$ and $y$, the system is inconsistent and has no solution.

---

### Conclusion

* **System 1:** **One solution** — every unknown column has a pivot ($r = 2 = n$), yielding $(x, y) = (1, 1)$.
* **System 2:** **Infinitely many solutions** — elimination produces a zero row $(0 \;\; 0 \mid 0)$, leaving $1$ free variable.
* **System 3:** **No solution** — elimination produces a contradictory row $(0 \;\; 0 \mid 1)$, corresponding to $0 = 1$.
