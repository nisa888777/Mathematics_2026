# Exercise 12. Intersection Line of Two Planes

## Question

Find a parametric equation of the line that is the intersection of

$$
x + y + z = 3, \qquad x - y + z = 1.
$$

Find its direction vector in two ways: from the system of equations and from the cross product of the normal vectors. Compare the results.

---

## Solution

Two non-parallel planes $\Pi_1$ and $\Pi_2$ in $\mathbb{R}^3$ intersect along a line $L$. Any point on $L$ simultaneously satisfies both plane equations, and the direction vector $v$ of $L$ is perpendicular to both normal vectors $n_1$ and $n_2$.

---

### 1. Method 1 — Solve the System of Equations (Algebraic Approach)

Write the linear system of the two planes:

$$
\begin{cases}
x + y + z = 3 & \text{(Equation 1)} \\
x - y + z = 1 & \text{(Equation 2)}
\end{cases}
$$

* **Step 1 — Eliminate $y$ by adding Equations 1 and 2:**

$$
(x + y + z) + (x - y + z) = 3 + 1 \implies 2x + 2z = 4 \implies x + z = 2
$$

* **Step 2 — Solve for $y$ by subtracting Equation 2 from Equation 1:**

$$
(x + y + z) - (x - y + z) = 3 - 1 \implies 2y = 2 \implies y = 1
$$

* **Step 3 — Introduce a free parameter $t = z \in \mathbb{R}$:**

From $x + z = 2$, we obtain $x = 2 - t$. Combined with $y = 1$ and $z = t$, the parametric coordinates of the intersection line are:

$$
\begin{cases}
x = 2 - t \\
y = 1 \\
z = t
\end{cases}, \qquad t \in \mathbb{R}
$$

In vector form, this gives the parametric equation of the intersection line:

$$
L: (x, y, z) = (2, 1, 0) + t(-1, 0, 1), \qquad t \in \mathbb{R}
$$

* **Direction vector from the system:** $v_{\text{alg}} = (-1, 0, 1)$, passing through the base point $P_0 = (2, 1, 0)$.

---

### 2. Method 2 — Cross Product of the Normal Vectors (Geometric Approach)

Read the normal vectors from $\Pi_1: x + y + z = 3$ and $\Pi_2: x - y + z = 1$:

$$
n_1 = (1, 1, 1), \qquad n_2 = (1, -1, 1)
$$

Because $n_1$ and $n_2$ are not scalar multiples, the planes are not parallel. Since $L$ lies in both $\Pi_1$ and $\Pi_2$, its direction is orthogonal to both $n_1$ and $n_2$, so we compute $v_{\text{geo}} = n_1 \times n_2$:

* **First component:** $(1)(1) - (1)(-1) = 1 - (-1) = 2$
* **Second component:** $(1)(1) - (1)(1) = 1 - 1 = 0$
* **Third component:** $(1)(-1) - (1)(1) = -1 - 1 = -2$

Thus, the direction vector obtained from the cross product is:

$$
v_{\text{geo}} = n_1 \times n_2 = (2, 0, -2)
$$

* **Orthogonality check:**
  * $v_{\text{geo}} \cdot n_1 = (2)(1) + (0)(1) + (-2)(1) = 2 + 0 - 2 = 0 \quad \checkmark$
  * $v_{\text{geo}} \cdot n_2 = (2)(1) + (0)(-1) + (-2)(1) = 2 + 0 - 2 = 0 \quad \checkmark$

Using the same base point $P_0 = (2, 1, 0)$ (found by setting $z = 0$ in the system), the geometric approach yields:

$$
L: (x, y, z) = (2, 1, 0) + s(2, 0, -2), \qquad s \in \mathbb{R}
$$

---

### 3. Compare the Two Results

Compare $v_{\text{alg}} = (-1, 0, 1)$ and $v_{\text{geo}} = (2, 0, -2)$:

$$
v_{\text{geo}} = (2, 0, -2) = -2(-1, 0, 1) = -2 v_{\text{alg}}
$$

* **Collinearity (Same Direction Line):** The two vectors are **nonzero scalar multiples** of one another ($v_{\text{geo}} = -2 v_{\text{alg}}$), so they span the exact same 1-dimensional direction subspace in $\mathbb{R}^3$.
* **Parameter Reparametrization:** Replacing $t = -2s$ transforms $(2, 1, 0) + t(-1, 0, 1)$ directly into $(2, 1, 0) + s(2, 0, -2)$, confirming that both parametric equations trace the **exact same line** in space.
* **Difference in Scale and Orientation:** The algebraic method naturally produces a simplified integer direction vector $(-1, 0, 1)$ with unit $z$-step, whereas the cross product produces $(2, 0, -2)$, whose magnitude $\|n_1 \times n_2\| = \sqrt{8} = 2\sqrt{2}$ also encodes the sine of the angle between $n_1$ and $n_2$ and follows the right-hand rule orientation.

---

### 4. Verify the Intersection Line in Both Planes

Substitute $(x(t), y(t), z(t)) = (2 - t, \, 1, \, t)$ into both original plane equations:

* **In $\Pi_1: x + y + z = 3$:**

$$
(2 - t) + 1 + t = 3 \implies 3 = 3 \quad \checkmark
$$

* **In $\Pi_2: x - y + z = 1$:**

$$
(2 - t) - 1 + t = 1 \implies 1 = 1 \quad \checkmark
$$

Both equations hold identically for all $t \in \mathbb{R}$.

---

### Conclusion

* **Parametric equation of the intersection line:** $(x, y, z) = (2, 1, 0) + t(-1, 0, 1)$, $t \in \mathbb{R}$ (equivalently, $(2, 1, 0) + s(2, 0, -2)$, $s \in \mathbb{R}$).
* **Direction vector (system of equations):** $v_{\text{alg}} = (-1, 0, 1)$.
* **Direction vector (cross product):** $v_{\text{geo}} = n_1 \times n_2 = (2, 0, -2)$.
* **Comparison:** $v_{\text{geo}} = -2 v_{\text{alg}}$; the vectors are nonzero scalar multiples pointing along the same line in opposite orientations with different lengths, defining the exact same geometric line.
