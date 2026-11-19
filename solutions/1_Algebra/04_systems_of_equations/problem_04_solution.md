# Exercise 4. Infinitely Many Solutions

## Question

Solve

$$
\begin{cases}
x + y + z = 2, \\\
2x + 2y + 2z = 4, \\\
x - y + z = 0.
\end{cases}
$$

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

---

## Solution

We form the augmented matrix for the $3 \times 3$ linear system[span_1](start_span)[span_1](end_span):

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 2 \\\ 2 & 2 & 2 & 4 \\\ 1 & -1 & 1 & 0 \end{array} \right)
$$

---

### 1. Reduce to Row Echelon Form

**Step 1: Eliminate the entries below the first pivot ($R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$)**

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 2 \\\ 0 & 0 & 0 & 0 \\\ 0 & -2 & 0 & -2 \end{array} \right)
$$

**Step 2: Swap Row 2 and Row 3 ($R_2 \leftrightarrow R_3$) and scale Row 2 ($R_2 \leftarrow -\frac{1}{2}R_2$)**

$$
\left( \begin{array}{ccc|c} 1 & 1 & 1 & 2 \\\ 0 & 1 & 0 & 1 \\\ 0 & 0 & 0 & 0 \end{array} \right)
$$

**Step 3: Eliminate the entry above the second pivot ($R_1 \leftarrow R_1 - R_2$)**

$$
\left( \begin{array}{ccc|c} 1 & 0 & 1 & 1 \\\ 0 & 1 & 0 & 1 \\\ 0 & 0 & 0 & 0 \end{array} \right)
$$

---

### 2. Identify the Free Variable and Write the Parametric Form

* **Pivot variables:** $x$ (column 1) and $y$ (column 2) are leading variables.
* **Free variable:** Column 3 has no pivot, so **$z$ is the free variable**. Let $z = t$, where $t \in \mathbb{R}$ is any real parameter.

Reading the equations from the reduced matrix:

$$
\begin{aligned}
x + z = 1 &\implies x = 1 - t \\\
y = 1 &\implies y = 1 \\\
z = t
\end{aligned}
$$

Thus, the general solution in parametric form is:

$$
\begin{pmatrix} x \\\ y \\\ z \end{pmatrix} = \begin{pmatrix} 1 - t \\\ 1 \\\ t \end{pmatrix} = \begin{pmatrix} 1 \\\ 1 \\\ 0 \end{pmatrix} + t \begin{pmatrix} -1 \\\ 0 \\\ 1 \end{pmatrix}, \qquad t \in \mathbb{R}
$$

---

### 3. Check for a Chosen Parameter Value

Choose $t = 2$. Substituting $t = 2$ into the parametric formula gives the point:

$$
(x, y, z) = (1 - 2, \, 1, \, 2) = (-1, 1, 2)
$$

Substituting $(x, y, z) = (-1, 1, 2)$ into all three original equations[span_2](start_span)[span_2](end_span):

1. **Equation 1:** $(-1) + 1 + 2 = 2 \quad \checkmark$
2. **Equation 2:** $2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4 \quad \checkmark$
3. **Equation 3:** $(-1) - 1 + 2 = 0 \quad \checkmark$

All three equations hold, confirming the parametric solution.

---

### Conclusion

* **Free variable:** $z = t \in \mathbb{R}$.
* **Parametric solution:** $(x, y, z) = (1 - t, \, 1, \, t)$ for any $t \in \mathbb{R}$.
* **Verification:** Choosing $t = 2$ gives $(-1, 1, 2)$, which satisfies every equation in the system[span_3](start_span)[span_3](end_span).
