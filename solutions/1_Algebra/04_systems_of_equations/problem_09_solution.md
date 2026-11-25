# Exercise 9. A System from a Sum Condition

## Question

Find numbers $x, y$ satisfying

$$
x + y = 10, \qquad 2x + 5y = 32.
$$

Solve the system and explain geometrically why the solution is unique.

---

## Solution

We write the system of two linear equations in two unknowns:

$$
\begin{cases}
x + y = 10, \\\
2x + 5y = 32.
\end{cases}
$$

---

### 1. Solve the System via Gaussian Elimination

Form the $2 \times 3$ augmented matrix:

$$
\left( \begin{array}{cc|c} 1 & 1 & 10 \\\ 2 & 5 & 32 \end{array} \right)
$$

* **Step 1: Eliminate $x$ from Row 2 ($R_2 \leftarrow R_2 - 2R_1$)**

$$
\left( \begin{array}{cc|c} 1 & 1 & 10 \\\ 0 & 3 & 12 \end{array} \right)
$$

* **Step 2: Back-Substitution**

From Row 2 ($3y = 12$):

$$
y = \frac{12}{3} = 4
$$

Substitute $y = 4$ into Row 1 ($x + y = 10$):

$$
x + 4 = 10 \quad \Longrightarrow \quad x = 6
$$

* **Verification:** Checking both original equations confirms $6 + 4 = 10$ and $2(6) + 5(4) = 12 + 20 = 32$.

Thus, the numbers are $x = 6$ and $y = 4$, giving the unique solution $(x, y) = (6, 4)$.

---

### 2. Geometric Explanation of Uniqueness

In the two-dimensional Cartesian plane ($\mathbb{R}^2$), each linear equation represents a straight line:

* **Line 1 ($x + y = 10$):** Rewriting in slope-intercept form gives $y = -x + 10$, which has slope $m_1 = -1$.
* **Line 2 ($2x + 5y = 32$):** Rewriting in slope-intercept form gives $y = -\frac{2}{5}x + \frac{32}{5}$, which has slope $m_2 = -\frac{2}{5}$.

Because the two lines have **different slopes** ($m_1 = -1 \neq -\frac{2}{5} = m_2$), they are neither parallel nor coincident. Two non-parallel lines in a plane must intersect at **exactly one point**, which corresponds algebraically to the unique solution $(x, y) = (6, 4)$.

---

### Conclusion

* **Solution:** $(x, y) = (6, 4)$ (so $x = 6$ and $y = 4$).
* **Geometric reason for uniqueness:** The two equations define straight lines in $\mathbb{R}^2$ with distinct slopes ($m_1 = -1$ and $m_2 = -\frac{2}{5}$), so they intersect at a single unique point $(6, 4)$.
