# Exercise 5. Row Echelon Form and Number of Solutions

## Question

For the augmented matrix

$$
\left( \begin{array}{ccc|c} 1 & 2 & -1 & 3 \\\ 0 & 1 & 2 & 1 \\\ 0 & 0 & 0 & 0 \end{array} \right)
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

---

## Solution

We examine the given $3 \times 4$ augmented matrix in row echelon form:

$$
\left( \begin{array}{ccc|c} 1 & 2 & -1 & 3 \\\ 0 & 1 & 2 & 1 \\\ 0 & 0 & 0 & 0 \end{array} \right)
$$

---

### 1. Number of Solutions and Free Variables

* **Consistency check:** The last row represents the equation $0x_1 + 0x_2 + 0x_3 = 0$, which is always satisfied. Since there is no inconsistent row of the form $(0 \;\; 0 \;\; 0 \mid c)$ with $c \neq 0$, the system is **consistent**.
* **How many variables may be chosen freely:** There are $n = 3$ unknowns ($x_1, x_2, x_3$) and $r = 2$ non-zero pivot rows (leading $1$s in Column 1 and Column 2). The number of free variables equals the number of non-pivot columns:

$$
\text{Number of free variables} = n - r = 3 - 2 = 1
$$

Because Column 3 does not contain a pivot, **$x_3$ may be chosen freely** ($1$ free variable). Since a free real parameter can take infinitely many values, the system has **infinitely many solutions**.

---

### 2. Parametric Form of the Solutions

Let the free variable be $x_3 = t$, where $t \in \mathbb{R}$. Solving for the pivot variables $x_2$ and $x_1$ by back-substitution:

* From Row 2 ($x_2 + 2x_3 = 1$):

$$
x_2 = 1 - 2x_3 = 1 - 2t
$$

* From Row 1 ($x_1 + 2x_2 - x_3 = 3$):

$$
x_1 = 3 - 2x_2 + x_3 = 3 - 2(1 - 2t) + t = 3 - 2 + 4t + t = 1 + 5t
$$

In vector parametric form, the solution set is:

$$
\begin{pmatrix} x_1 \\\ x_2 \\\ x_3 \end{pmatrix} = \begin{pmatrix} 1 + 5t \\\ 1 - 2t \\\ t \end{pmatrix} = \begin{pmatrix} 1 \\\ 1 \\\ 0 \end{pmatrix} + t \begin{pmatrix} 5 \\\ -2 \\\ 1 \end{pmatrix}, \qquad t \in \mathbb{R}
$$

---

### Conclusion

* **Number of solutions:** Infinitely many solutions (the system is consistent and has $1$ free variable).
* **Free variables:** $n - r = 3 - 2 = 1$ variable ($x_3 = t \in \mathbb{R}$) may be chosen freely because Column 3 lacks a pivot.
* **Parametric form:** $(x_1, x_2, x_3) = (1 + 5t, \, 1 - 2t, \, t)$ for $t \in \mathbb{R}$.
