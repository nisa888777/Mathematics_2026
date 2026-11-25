# Exercise 6. Projection and Perpendicular Component

## Question

Find the projection of $u = (4, 2)$ onto the direction $v = (1, 1)$. Then compute

$$
r = u - \text{proj}_{v} u
$$

and verify that $r \cdot v = 0$. Explain this result geometrically.

---

## Solution

In $\mathbb{R}^2$, any vector $u$ can be decomposed relative to a nonzero vector $v$ into a component parallel to $v$ and a component orthogonal (perpendicular) to $v$:

$$
u = \text{proj}_{v} u + r
$$

* **Orthogonal Projection Mechanism:** The orthogonal projection of $u$ onto $v$ is given by:

$$
\text{proj}_{v} u = \frac{u \cdot v}{v \cdot v} v = \frac{u \cdot v}{\|v\|^2} v
$$

---

### 1. Compute the Projection $\text{proj}_{v} u$

* **Step 1 — Compute the dot products $u \cdot v$ and $v \cdot v$:**

$$
u \cdot v = (4)(1) + (2)(1) = 4 + 2 = 6
$$

$$
v \cdot v = \|v\|^2 = 1^2 + 1^2 = 1 + 1 = 2
$$

* **Step 2 — Scale $v$ by $\frac{u \cdot v}{v \cdot v}$:**

$$
\text{proj}_{v} u = \frac{6}{2}(1, 1) = 3(1, 1) = (3, 3)
$$

---

### 2. Compute the Perpendicular Component $r = u - \text{proj}_{v} u$

Subtract $\text{proj}_{v} u = (3, 3)$ from $u = (4, 2)$ component-wise:

$$
r = u - \text{proj}_{v} u = (4, 2) - (3, 3) = (4 - 3, \, 2 - 3) = (1, -1)
$$

---

### 3. Verify That $r \cdot v = 0$

Compute the Euclidean dot product of $r = (1, -1)$ and $v = (1, 1)$:

$$
r \cdot v = (1)(1) + (-1)(1) = 1 - 1 = 0
$$

Since $r \cdot v = 0$ and both vectors are nonzero, $r$ is confirmed to be **perpendicular** ($r \perp v$) to the direction of $v$.

---

### 4. Geometric Explanation

Geometrically in $\mathbb{R}^2$, dropping a perpendicular line from the tip of $u = (4, 2)$ onto the line spanned by $v = (1, 1)$ (the line $y = x$) divides $u$ into two orthogonal legs of a right triangle:

* **Parallel component ($\text{proj}_{v} u = (3, 3)$):** The shadow cast by $u$ along the line $y = x$, which is a scalar multiple ($3v$) of $v$.
* **Perpendicular (residual) component ($r = (1, -1)$):** The shortest displacement vector connecting the line $y = x$ at $(3, 3)$ directly to the tip of $u$ at $(4, 2)$. Because the shortest path from a point to a line meets that line at a $90^\circ$ angle, $r$ must be orthogonal to $v$, giving $r \cdot v = 0$ and satisfying the Pythagorean identity $\|u\|^2 = \|\text{proj}_{v} u\|^2 + \|r\|^2$ ($20 = 18 + 2$).

---

### Conclusion

* **Projection onto $v$:** $\text{proj}_{v} u = (3, 3)$.
* **Perpendicular component:** $r = (1, -1)$.
* **Orthogonality verification:** $r \cdot v = (1)(1) + (-1)(1) = 0$, confirming that $u = (3, 3) + (1, -1)$ decomposes $u$ into a component parallel to $v$ and a component perpendicular to $v$.
