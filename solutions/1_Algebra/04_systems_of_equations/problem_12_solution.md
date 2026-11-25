# Exercise 12. Homogeneous System

## Question

Solve

$$
\begin{cases}
x + 2y - z = 0, \\
2x + 4y - 2z = 0, \\
x - y + 2z = 0.
\end{cases}
$$

Give all solutions in parametric form and explain why $(0, 0, 0)$ always satisfies a homogeneous system.

---

## Solution

We form the $3 \times 4$ augmented matrix for the homogeneous linear system:

$$
\left( \begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 2 & 4 & -2 & 0 \\ 1 & -1 & 2 & 0 \end{array} \right)
$$

---

### 1. Reduce to Row Echelon Form

* **Step 1:** Eliminate $x$ from Row 2 ($R_2 \leftarrow R_2 - 2R_1$) and Row 3 ($R_3 \leftarrow R_3 - R_1$):

$$
\left( \begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & -3 & 3 & 0 \end{array} \right)
$$

* **Step 2:** Swap Row 2 and Row 3 ($R_2 \leftrightarrow R_3$) so that the zero row moves to the bottom:

$$
\left( \begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & -3 & 3 & 0 \\ 0 & 0 & 0 & 0 \end{array} \right)
$$

* **Step 3:** Scale Row 2 ($R_2 \leftarrow -\frac{1}{3}R_2$) to obtain a leading $1$ in the second pivot:

$$
\left( \begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 1 & -1 & 0 \\ 0 & 0 & 0 & 0 \end{array} \right)
$$

---

### 2. Parametric Form of All Solutions

There are $n = 3$ unknowns ($x, y, z$) and $r = 2$ pivots (in Column 1 and Column 2). Column 3 has no pivot, so **$z$ is a free variable**. Let $z = t$, where $t \in \mathbb{R}$.

Solving for the pivot variables $y$ and $x$ by back-substitution:

* From Row 2 ($y - z = 0$):

$$
y = z = t
$$

* From Row 1 ($x + 2y - z = 0$):

$$
x = -2y + z = -2t + t = -t
$$

In vector parametric form, all solutions are given by:

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} -t \\ t \\ t \end{pmatrix} = t \begin{pmatrix} -1 \\ 1 \\ 1 \end{pmatrix}, \qquad t \in \mathbb{R}
$$

---

### 3. Why $(0, 0, 0)$ Always Satisfies a Homogeneous System

A homogeneous linear system has the general matrix form $Ax = 0$, meaning every equation has the form:

$$
a_{i1}x + a_{i2}y + a_{i3}z = 0
$$

with a zero constant term on the right-hand side. Substituting $(x, y, z) = (0, 0, 0)$ into any linear equation without a constant term evaluates the left-hand side to:

$$
a_{i1}(0) + a_{i2}(0) + a_{i3}(0) = 0 + 0 + 0 = 0
$$

which identically equals the right-hand side ($0 = 0$) regardless of the values of the coefficients $a_{ij}$. Therefore, the trivial solution $(0, 0, 0)$ always satisfies every equation in a homogeneous system (and corresponds to setting the parameter $t = 0$ in our parametric solution).

---

### Conclusion

* **Parametric form:** $(x, y, z) = (-t, \, t, \, t) = t(-1, 1, 1)$ for $t \in \mathbb{R}$ (infinitely many solutions).
* **Trivial solution:** Substituting $(0, 0, 0)$ into $Ax = 0$ yields $A \cdot 0 = 0$, so every equation reduces to $0 = 0$ and is automatically satisfied.
