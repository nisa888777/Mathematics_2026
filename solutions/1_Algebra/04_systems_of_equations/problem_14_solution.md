# Exercise 14. A Small Change in the Right-Hand Side

## Question

Compare the systems

$$
\begin{cases}
x + y = 2, \\\
2x - y = 1, \\\
3x = 3
\end{cases}
$$

and

$$
\begin{cases}
x + y = 2, \\\
2x - y = 1, \\\
3x = 3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

---

## Solution

Both systems are overdetermined ($3$ linear equations in $2$ unknowns $x, y$) and share the exact same $3 \times 2$ coefficient matrix:

$$
A = \begin{pmatrix} 1 & 1 \\\ 2 & -1 \\\ 3 & 0 \end{pmatrix}
$$

---

### 1. Consistency Check for the First System

Form the $3 \times 3$ augmented matrix for the first system:

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 2 & -1 & 1 \\\ 3 & 0 & 3 \end{array} \right)
$$

* **Step 1:** Eliminate $x$ from Row 2 ($R_2 \leftarrow R_2 - 2R_1$) and Row 3 ($R_3 \leftarrow R_3 - 3R_1$):

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 0 & -3 & -3 \\\ 0 & -3 & -3 \end{array} \right)
$$

* **Step 2:** Eliminate $y$ from Row 3 ($R_3 \leftarrow R_3 - R_2$) and scale Row 2 ($R_2 \leftarrow -\frac{1}{3}R_2$):

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 0 & 1 & 1 \\\ 0 & 0 & 0 \end{array} \right)
$$

Row 3 reduces to $0x + 0y = 0$, which is satisfied identically. Back-substituting $y = 1$ into Row 1 ($x + 1 = 2$) gives $x = 1$. Thus, the first system is **consistent** and has the unique solution $(x, y) = (1, 1)$.

---

### 2. Consistency Check for the Second System

Form the $3 \times 3$ augmented matrix for the second system:

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 2 & -1 & 1 \\\ 3 & 0 & 3.1 \end{array} \right)
$$

* **Step 1:** Eliminate $x$ from Row 2 ($R_2 \leftarrow R_2 - 2R_1$) and Row 3 ($R_3 \leftarrow R_3 - 3R_1$):

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 0 & -3 & -3 \\\ 0 & -3 & -2.9 \end{array} \right)
$$

* **Step 2:** Eliminate $y$ from Row 3 ($R_3 \leftarrow R_3 - R_2$):

$$
\left( \begin{array}{cc|c} 1 & 1 & 2 \\\ 0 & -3 & -3 \\\ 0 & 0 & 0.1 \end{array} \right)
$$

Row 3 represents the equation $0x + 0y = 0.1$ ($0 = 0.1$), which is a contradiction. Thus, the second system is **inconsistent** and has **no solution**.

---

### 3. Why a Small Change in One Number Changes the System Type

* **Algebraic reason:** Notice that the left-hand side of the third equation is the sum of the left-hand sides of the first two equations:

$$
(x + y) + (2x - y) = 3x
$$

For the system to be consistent, the right-hand side of the third equation must equal the exact sum of the first two right-hand sides ($2 + 1 = 3$). In the first system, $3 = 3$ holds, so the third equation is redundant. In the second system, changing $3$ to $3.1$ breaks this exact linear compatibility condition ($3.1 \neq 3$), turning a redundant equation into a contradiction ($0 = 0.1$).

* **Geometric reason:** In $\mathbb{R}^2$, the first two lines ($x + y = 2$ and $2x - y = 1$) intersect at a single point $(1, 1)$. In the first system, the third line ($3x = 3$, i.e., $x = 1$) passes directly through that intersection point. Shifting the right-hand side to $3.1$ moves the third line to $x = \frac{3.1}{3} = 1.033\dots$, which misses the intersection point $(1, 1)$, so all three lines no longer share any common point.

---

### Conclusion

* **First system:** **Consistent** with a unique solution $(x, y) = (1, 1)$.
* **Second system:** **Inconsistent** (no solution), because elimination produces the contradictory row $(0 \;\; 0 \mid 0.1)$.
* **Explanation:** Because the third left-hand side is a linear combination of the first two ($E_1 + E_2 = 3x$), consistency requires the third right-hand side to equal $2 + 1 = 3$ exactly; any perturbation (such as $3.1$) violates this exact condition and makes the overdetermined system inconsistent.
