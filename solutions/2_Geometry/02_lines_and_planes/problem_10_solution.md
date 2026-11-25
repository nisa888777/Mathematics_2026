# Exercise 10. Projection of a Point onto a Plane

## Question

Find the orthogonal projection of $P = (2, 1, 3)$ onto the plane $x + y + z = 3$, and then find the reflection of $P$ across this plane. Check that the midpoint of the segment joining the point and its reflection lies on the plane.

---

## Solution

To find the orthogonal projection $P_{\text{proj}}$ of a point $P$ onto a plane $\Pi: n \cdot X = d$, we construct the line $L$ passing through $P$ in the direction of the plane's normal vector $n$ and intersect $L$ with $\Pi$. The reflection $P'$ across $\Pi$ is then obtained by continuing an equal displacement beyond $P_{\text{proj}}$ along the same normal line.

---

### 1. Construct the Normal Line Through $P$ and Intersect With $\Pi$

* **Given data:**
  * Point: $P = (2, 1, 3)$
  * Plane: $\Pi: x + y + z = 3$, with normal vector $n = (1, 1, 1)$

* **Step 1 — Write the parametric equation of the normal line $L$ through $P$:**

$$
L: (x, y, z) = (2, 1, 3) + t(1, 1, 1) \iff
\begin{cases}
x(t) = 2 + t \\
y(t) = 1 + t \\
z(t) = 3 + t
\end{cases}, \qquad t \in \mathbb{R}
$$

* **Step 2 — Substitute into $\Pi: x + y + z = 3$ to find $t$:**

$$
(2 + t) + (1 + t) + (3 + t) = 3
$$

$$
6 + 3t = 3 \implies 3t = -3 \implies t = -1
$$

* **Step 3 — Evaluate $L$ at $t = -1$ to obtain the orthogonal projection $P_{\text{proj}}$:**

$$
P_{\text{proj}} = (2, 1, 3) + (-1)(1, 1, 1) = (2 - 1, \, 1 - 1, \, 3 - 1) = (1, 0, 2)
$$

* **Projection verification:**
  * **On $\Pi$:** $1 + 0 + 2 = 3 \quad \checkmark$
  * **Orthogonal residual:** $\overrightarrow{P_{\text{proj}} P} = P - P_{\text{proj}} = (1, 1, 1)$, which is parallel to $n = (1, 1, 1)$ and hence perpendicular to $\Pi$.

---

### 2. Find the Reflection $P'$ of $P$ Across the Plane

Because $P_{\text{proj}}$ is the midpoint of the segment $\overline{P P'}$, we have:

$$
P_{\text{proj}} = \frac{P + P'}{2} \implies P' = 2 P_{\text{proj}} - P
$$

Equivalently, since $P_{\text{proj}}$ corresponds to $t = -1$ along the normal line $L$, the reflection $P'$ corresponds to $t = 2(-1) = -2$:

$$
P' = 2(1, 0, 2) - (2, 1, 3) = (2 - 2, \, 0 - 1, \, 4 - 3) = (0, -1, 1)
$$

---

### 3. Check That the Midpoint Lies on the Plane

Compute the midpoint $M$ of the line segment joining $P = (2, 1, 3)$ and $P' = (0, -1, 1)$:

$$
M = \frac{P + P'}{2} = \left(\frac{2 + 0}{2}, \; \frac{1 + (-1)}{2}, \; \frac{3 + 1}{2}\right) = \left(\frac{2}{2}, \; \frac{0}{2}, \; \frac{4}{2}\right) = (1, 0, 2)
$$

Notice that $M = (1, 0, 2) = P_{\text{proj}}$. Substitute $M = (1, 0, 2)$ into the plane equation $x + y + z = 3$:

$$
1 + 0 + 2 = 3 \quad \checkmark
$$

Additionally, the displacement vector $\overrightarrow{P' P} = P - P' = (2, 2, 2) = 2(1, 1, 1) = 2n$ is perpendicular to $\Pi$, confirming that $P'$ is the exact mirror reflection of $P$ across $x + y + z = 3$.

---

### Conclusion

* **Orthogonal projection:** $P_{\text{proj}} = (1, 0, 2)$.
* **Reflection across $x + y + z = 3$:** $P' = (0, -1, 1)$.
* **Midpoint verification:** The midpoint of $\overline{P P'}$ is $M = (1, 0, 2) = P_{\text{proj}}$, which satisfies $1 + 0 + 2 = 3$ and therefore lies on the plane.
