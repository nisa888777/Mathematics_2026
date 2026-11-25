# Exercise 8. Linear Combination and Checking the Result

## Question

Check whether $w = (5, 1)$ can be written as

$$
w = au + bv,
$$

where $u = (1, 1)$ and $v = (2, -1)$. If so, find $a, b$, reconstruct $w$ from them, and explain the geometric meaning of the existence of such coefficients.

---

## Solution

To determine whether $w$ is a **linear combination** of $u$ and $v$, we equate components to convert the vector equation $w = au + bv$ into a $2 \times 2$ **system of linear equations** for the unknown scalars $a, b \in \mathbb{R}$.

---

### 1. Set Up the System and Find $a, b$

* **Step 1 — Expand the vector equation component-wise:**

$$
(5, 1) = a(1, 1) + b(2, -1) = (a + 2b, \, a - b)
$$

* **Step 2 — Equate corresponding coordinates:**

$$
\begin{cases}
a + 2b = 5 & \text{(Equation 1)} \\
a - b = 1 & \text{(Equation 2)}
\end{cases}
$$

* **Step 3 — Solve for $a$ and $b$ by elimination:** Subtract Equation 2 from Equation 1 to eliminate $a$:

$$
(a + 2b) - (a - b) = 5 - 1 \implies 3b = 4 \implies b = \frac{4}{3}
$$

Substitute $b = \frac{4}{3}$ back into Equation 2 ($a - b = 1$):

$$
a - \frac{4}{3} = 1 \implies a = 1 + \frac{4}{3} = \frac{7}{3}
$$

Since a unique real solution $(a, b) = \left(\frac{7}{3}, \, \frac{4}{3}\right)$ exists, $w$ **can** be written as a linear combination of $u$ and $v$.

---

### 2. Reconstruct $w$ From $a = \frac{7}{3}$ and $b = \frac{4}{3}$

Substitute $a = \frac{7}{3}$ and $b = \frac{4}{3}$ into $au + bv$:

$$
au + bv = \frac{7}{3}(1, 1) + \frac{4}{3}(2, -1) = \left(\frac{7}{3}, \, \frac{7}{3}\right) + \left(\frac{8}{3}, \, -\frac{4}{3}\right) = \left(\frac{7 + 8}{3}, \, \frac{7 - 4}{3}\right) = \left(\frac{15}{3}, \, \frac{3}{3}\right) = (5, 1) = w
$$

This confirms that $w = \frac{7}{3}u + \frac{4}{3}v$.

---

### 3. Geometric Meaning of the Existence of Such Coefficients

* **Spanning the Plane ($\mathbb{R}^2$):** Because $u = (1, 1)$ and $v = (2, -1)$ are not scalar multiples of one another, they point along two distinct non-parallel lines through the origin. As a result, they form a **basis** for $\mathbb{R}^2$, meaning their linear combinations span the entire two-dimensional plane ($\text{span}\{u, v\} = \mathbb{R}^2$).
* **Parallelogram / Skew-Grid Coordinates:** Geometrically, the existence of $a = \frac{7}{3}$ and $b = \frac{4}{3}$ means we can reach the target point $(5, 1)$ starting from the origin by moving $\frac{7}{3}$ units along the direction of $u$ and then $\frac{4}{3}$ units parallel to the direction of $v$ (forming the diagonal of a parallelogram with scaled sides $\frac{7}{3}u$ and $\frac{4}{3}v$). Moreover, because $u$ and $v$ are linearly independent, this path—and hence the pair of coefficients $(a, b)$—is **unique**.

---

### Conclusion

* **Existence and coefficients:** Yes, $w = au + bv$ holds with unique scalars $a = \frac{7}{3}$ and $b = \frac{4}{3}$.
* **Reconstruction:** $\frac{7}{3}(1, 1) + \frac{4}{3}(2, -1) = \left(\frac{15}{3}, \, \frac{3}{3}\right) = (5, 1) = w$.
* **Geometric meaning:** Because $u$ and $v$ point in independent directions, they span all of $\mathbb{R}^2$, allowing $w$ to be reached uniquely as the diagonal of the parallelogram formed by scaling $u$ by $\frac{7}{3}$ and $v$ by $\frac{4}{3}$.
