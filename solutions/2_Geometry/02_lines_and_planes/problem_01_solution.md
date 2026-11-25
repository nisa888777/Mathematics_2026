# Exercise 1. Line Through Two Points

## Question

Find the equation of the line through $A = (1, 2)$ and $B = (4, -1)$ in parametric and general form. Identify a direction vector and an example of a normal vector. Check that both points satisfy the equation you obtain.

---

## Solution

In $\mathbb{R}^2$, a line passing through two distinct points $A = (x_0, y_0)$ and $B = (x_1, y_1)$ is uniquely determined by a base point (such as $A$) and a **direction vector** $v = \overrightarrow{AB}$:

$$
\mathbf{r}(t) = A + t v, \qquad t \in \mathbb{R}
$$

---

### 1. Identify a Direction Vector and Write the Parametric Form

* **Step 1 — Construct a direction vector $v$:** Subtract the coordinates of $A = (1, 2)$ from $B = (4, -1)$:

$$
v = \overrightarrow{AB} = B - A = (4 - 1, \, -1 - 2) = (3, -3)
$$

*(Note: Any nonzero scalar multiple of $(3, -3)$, such as $v_{\text{simp}} = \frac{1}{3}(3, -3) = (1, -1)$, is also a valid direction vector for the same line.)*

* **Step 2 — Write the parametric equations:** Using the base point $A = (1, 2)$ and direction vector $v = (3, -3)$:

$$
\begin{cases}
x(t) = 1 + 3t \\
y(t) = 2 - 3t
\end{cases}, \qquad t \in \mathbb{R}
$$

*(Equivalently, using the simplified direction vector $v_{\text{simp}} = (1, -1)$ gives $x(s) = 1 + s$ and $y(s) = 2 - s$ for $s \in \mathbb{R}$.)*

---

### 2. Find the General Form and Identify a Normal Vector

* **Step 1 — Eliminate the parameter $t$:** From the parametric system $x = 1 + 3t$ and $y = 2 - 3t$, add the two equations together so that $3t$ and $-3t$ cancel:

$$
x + y = (1 + 3t) + (2 - 3t) = 3 \implies x + y - 3 = 0
$$

Thus, the **general form** ($ax + by + c = 0$) of the line is:

$$
x + y - 3 = 0
$$

* **Step 2 — Identify a normal vector $n$:** In $\mathbb{R}^2$, the coefficients $(a, b)$ of $x$ and $y$ in the general equation $ax + by + c = 0$ directly give a **normal vector** perpendicular to the line:

$$
n = (1, 1)
$$

* **Orthogonality check between direction and normal vectors:**

$$
n \cdot v = (1)(3) + (1)(-3) = 3 - 3 = 0
$$

This confirms that $n = (1, 1)$ is perpendicular to the line's direction vector $v = (3, -3)$.

---

### 3. Check That Both Points $A$ and $B$ Satisfy the Equations

* **Check in the General Form ($x + y - 3 = 0$):**
  * **For $A = (1, 2)$:** $1 + 2 - 3 = 0 \implies 0 = 0$ (satisfied).
  * **For $B = (4, -1)$:** $4 + (-1) - 3 = 0 \implies 0 = 0$ (satisfied).

* **Check in the Parametric Form ($x(t) = 1 + 3t, \; y(t) = 2 - 3t$):**
  * **For $A = (1, 2)$:** Setting $t = 0$ yields $(x(0), y(0)) = (1 + 0, \, 2 - 0) = (1, 2) = A$.
  * **For $B = (4, -1)$:** Setting $t = 1$ yields $(x(1), y(1)) = (1 + 3, \, 2 - 3) = (4, -1) = B$.

---

### Conclusion

* **Parametric form:** $x = 1 + 3t, \; y = 2 - 3t$ ($t \in \mathbb{R}$), or equivalently $x = 1 + s, \; y = 2 - s$ ($s \in \mathbb{R}$).
* **General form:** $x + y - 3 = 0$.
* **Direction vector:** $v = (3, -3)$ (or simplified $v_{\text{simp}} = (1, -1)$).
* **Normal vector example:** $n = (1, 1)$ (satisfying $n \cdot v = 0$).
* **Point verification:** Both $A = (1, 2)$ and $B = (4, -1)$ satisfy $x + y - 3 = 0$ and correspond to $t = 0$ and $t = 1$ in the parametric equations.
