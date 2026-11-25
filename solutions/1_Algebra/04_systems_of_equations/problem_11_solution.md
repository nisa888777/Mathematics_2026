# Exercise 11. A Parameter in a System of Three Equations

## Question

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x + y + z = 1, \\\
x + ty + z = 2, \\\
x + y + tz = 3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

---

## Solution

We form the $3 \times 4$ augmented matrix for the linear system:

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 1 \\\ 1 & t & 1 & 2 \\\ 1 & 1 & t & 3 \end{array} \right)
$$

---

### 1. Forward Elimination

Perform the elementary row operations $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$ to eliminate $x$ below the first pivot:

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 1 \\\ 0 & t - 1 & 0 & 1 \\\ 0 & 0 & t - 1 & 2 \end{array} \right)
$$

The augmented matrix is already in upper-triangular (row echelon) form. The corresponding reduced system of equations is:

$$
\begin{cases}
x + y + z = 1, \\\
(t - 1)y = 1, \\\
(t - 1)z = 2.
\end{cases}
$$

---

### 2. Critical Parameter Value Where Standard Division Ceases to Be Valid

To solve the second and third equations for $y$ and $z$ by dividing by $(t - 1)$, we require $t - 1 \neq 0$, which means $t \neq 1$. Therefore, the standard division step ceases to be valid at the critical value **$t = 1$**.

---

### 3. Case-by-Case Analysis of the Number of Solutions

* **Case 1: $t = 1$ (Critical Value)**

Substituting $t = 1$ into the reduced augmented matrix gives:

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 1 \\\ 0 & 0 & 0 & 1 \\\ 0 & 0 & 0 & 2 \end{array} \right)
$$

Row 2 corresponds to $0x + 0y + 0z = 1$ ($0 = 1$) and Row 3 corresponds to $0x + 0y + 0z = 2$ ($0 = 2$). Both equations are contradictions, so the system is **inconsistent** and has **no solution** ($0$ solutions).

* **Case 2: $t \neq 1$ (General Case)**

Since $t - 1 \neq 0$, we can safely divide by $(t - 1)$ in Row 3 and Row 2 to find unique values for $z$ and $y$, and then substitute back into Row 1 for $x$:

$$
z = \frac{2}{t - 1}, \qquad y = \frac{1}{t - 1}
$$

$$
x = 1 - y - z = 1 - \frac{1}{t - 1} - \frac{2}{t - 1} = 1 - \frac{3}{t - 1} = \frac{t - 4}{t - 1}
$$

Because every variable is uniquely determined, the system is **consistent** and has a **unique solution** ($1$ solution):

$$
(x, y, z) = \left( \frac{t - 4}{t - 1}, \, \frac{1}{t - 1}, \, \frac{2}{t - 1} \right)
$$

---

### Conclusion

* **If $t = 1$:** Standard division by $(t - 1)$ is invalid, elimination yields contradictory rows ($0 = 1$ and $0 = 2$), and the system has **no solution**.
* **If $t \neq 1$:** The system has **exactly one unique solution**, given by $(x, y, z) = \left( \frac{t - 4}{t - 1}, \, \frac{1}{t - 1}, \, \frac{2}{t - 1} \right)$.
