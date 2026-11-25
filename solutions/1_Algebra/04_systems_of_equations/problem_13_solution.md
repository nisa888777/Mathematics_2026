# Exercise 13. Does Every Equation Add New Information?

## Question

Consider the system

$$
x_1 + x_2 = 10, \qquad x_2 + x_3 = 8, \qquad x_1 - x_3 = 2.
$$

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

---

## Solution

We form the $3 \times 4$ augmented matrix for the linear system:

$$
\left( \begin{array}{ccc|c} 1 & 1 & 0 & 10 \\\ 0 & 1 & 1 & 8 \\\ 1 & 0 & -1 & 2 \end{array} \right)
$$

---

### 1. Solve the System via Gaussian Elimination

* **Step 1:** Eliminate $x_1$ from Row 3 ($R_3 \leftarrow R_3 - R_1$):

$$
\left( \begin{array}{ccc|c} 1 & 1 & 0 & 10 \\\ 0 & 1 & 1 & 8 \\\ 0 & -1 & -1 & -8 \end{array} \right)
$$

* **Step 2:** Eliminate $x_2$ from Row 3 ($R_3 \leftarrow R_3 + R_2$):

$$
\left( \begin{array}{ccc|c} 1 & 1 & 0 & 10 \\\ 0 & 1 & 1 & 8 \\\ 0 & 0 & 0 & 0 \end{array} \right)
$$

* **Step 3:** Parametric Form of the Solution Set

There are $n = 3$ unknowns ($x_1, x_2, x_3$) and $r = 2$ non-zero pivot rows (in Column 1 and Column 2). Since Column 3 lacks a pivot, **$x_3$ is a free variable**. Let $x_3 = t$, where $t \in \mathbb{R}$.

Solving for $x_2$ and $x_1$ by back-substitution:

* From Row 2 ($x_2 + x_3 = 8$):

$$
x_2 = 8 - x_3 = 8 - t
$$

* From Row 1 ($x_1 + x_2 = 10$):

$$
x_1 = 10 - x_2 = 10 - (8 - t) = 2 + t
$$

In vector parametric form, the solution set is:

$$
\begin{pmatrix} x_1 \\\ x_2 \\\ x_3 \end{pmatrix} = \begin{pmatrix} 2 + t \\\ 8 - t \\\ t \end{pmatrix} = \begin{pmatrix} 2 \\\ 8 \\\ 0 \end{pmatrix} + t \begin{pmatrix} 1 \\\ -1 \\\ 1 \end{pmatrix}, \qquad t \in \mathbb{R}
$$

---

### 2. Independence Check and Derivation of the Redundant Equation

* **Are all three equations independently necessary?** **No.** During Gaussian elimination, the third row reduced completely to $(0 \;\; 0 \;\; 0 \mid 0)$, which indicates that the third equation is redundant and adds no new restriction to the solution set. Any two of the equations uniquely determine the exact same solution set.

* **Explicit derivation by calculation:** Subtracting the second equation ($E_2$) from the first equation ($E_1$) yields the third equation ($E_3$):

$$
\begin{aligned}
E_1 - E_2 &: \quad (x_1 + x_2) - (x_2 + x_3) = 10 - 8 \\\
&\Longrightarrow \quad x_1 + x_2 - x_2 - x_3 = 2 \\\
&\Longrightarrow \quad x_1 - x_3 = 2 \quad (E_3)
\end{aligned}
$$

Because $E_3 = E_1 - E_2$, the third equation is a linear combination of the first two and is automatically satisfied whenever the first two equations hold.

---

### Conclusion

* **Solution set:** $(x_1, x_2, x_3) = (2 + t, \, 8 - t, \, t)$ for $t \in \mathbb{R}$ (infinitely many solutions).
* **Redundancy:** Not all three equations are independently necessary; the third equation follows directly from subtracting the second equation from the first ($E_3 = E_1 - E_2$).
