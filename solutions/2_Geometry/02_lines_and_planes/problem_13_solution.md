# Exercise 13. Closest Point on a Plane

## Question

Find the point on the plane $x + 2y + 2z = 4$ closest to $P = (3, 0, 0)$. Give the distance and check that the segment joining the two points is perpendicular to the plane.

---

## Solution

The point $Q$ on a plane $\Pi: n \cdot X = d$ closest to an external point $P$ is the **orthogonal projection** of $P$ onto $\Pi$. It is obtained by intersecting the normal line $L$ passing through $P$ in the direction of $n$ with the plane $\Pi$, and the shortest distance is the Euclidean length $\|P - Q\|$.

---

### 1. Construct the Normal Line Through $P$ and Find the Closest Point $Q$

* **Given data:**
  * External point: $P = (3, 0, 0)$
  * Plane: $\Pi: x + 2y + 2z = 4$, with normal vector $n = (1, 2, 2)$

* **Step 1 — Write the parametric equation of the normal line $L$ through $P$:**

$$
L: (x, y, z) = (3, 0, 0) + t(1, 2, 2) \iff
\begin{cases}
x(t) = 3 + t \\
y(t) = 2t \\
z(t) = 2t
\end{cases}, \qquad t \in \mathbb{R}
$$

* **Step 2 — Substitute into $\Pi: x + 2y + 2z = 4$ to solve for $t$:**

$$
(3 + t) + 2(2t) + 2(2t) = 4
$$

$$
3 + t + 4t + 4t = 4 \implies 3 + 9t = 4 \implies 9t = 1 \implies t = \frac{1}{9}
$$

* **Step 3 — Evaluate $L$ at $t = \frac{1}{9}$ to obtain the closest point $Q$:**

$$
Q = (3, 0, 0) + \frac{1}{9}(1, 2, 2) = \left(3 + \frac{1}{9}, \; 0 + \frac{2}{9}, \; 0 + \frac{2}{9}\right) = \left(\frac{28}{9}, \; \frac{2}{9}, \; \frac{2}{9}\right)
$$

* **Plane membership check ($Q \in \Pi$):**

$$
\frac{28}{9} + 2\left(\frac{2}{9}\right) + 2\left(\frac{2}{9}\right) = \frac{28 + 4 + 4}{9} = \frac{36}{9} = 4 \quad \checkmark
$$

Thus, $Q = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right)$ lies on the plane $\Pi$.

---

### 2. Compute the Distance From $P$ to the Plane

* **Method 1 — Euclidean distance between $P = (3, 0, 0)$ and $Q = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right)$:**

First form the displacement vector $\overrightarrow{PQ} = Q - P$:

$$
\overrightarrow{PQ} = \left(\frac{28}{9} - 3, \; \frac{2}{9} - 0, \; \frac{2}{9} - 0\right) = \left(\frac{1}{9}, \; \frac{2}{9}, \; \frac{2}{9}\right)
$$

Take its Euclidean norm:

$$
d(P, \Pi) = \|\overrightarrow{PQ}\| = \sqrt{\left(\frac{1}{9}\right)^2 + \left(\frac{2}{9}\right)^2 + \left(\frac{2}{9}\right)^2} = \sqrt{\frac{1 + 4 + 4}{81}} = \sqrt{\frac{9}{81}} = \frac{3}{9} = \frac{1}{3}
$$

* **Method 2 — Direct point-to-plane distance formula verification:**

$$
d(P, \Pi) = \frac{|1(3) + 2(0) + 2(0) - 4|}{\sqrt{1^2 + 2^2 + 2^2}} = \frac{|3 - 4|}{\sqrt{1 + 4 + 4}} = \frac{1}{\sqrt{9}} = \frac{1}{3} \quad \checkmark
$$

---

### 3. Check That the Segment $\overline{PQ}$ Is Perpendicular to the Plane

A line segment $\overline{PQ}$ is perpendicular to the plane $\Pi$ if and only if its direction vector $\overrightarrow{PQ}$ is a nonzero scalar multiple of the plane's normal vector $n = (1, 2, 2)$ (or equivalently, orthogonal to every direction vector lying in $\Pi$):

$$
\overrightarrow{PQ} = \left(\frac{1}{9}, \; \frac{2}{9}, \; \frac{2}{9}\right) = \frac{1}{9}(1, 2, 2) = \frac{1}{9} n
$$

* **Collinearity with the normal:** Because $\overrightarrow{PQ} = \frac{1}{9} n$, the segment $\overline{PQ}$ points directly along the normal line to $\Pi$.
* **Orthogonality to in-plane directions:** For any two points $X, Y \in \Pi$, $n \cdot (X - Y) = 4 - 4 = 0$, so $\overrightarrow{PQ} \cdot (X - Y) = \frac{1}{9} n \cdot (X - Y) = 0$. Hence, $\overline{PQ}$ is perpendicular to every line in the plane $\Pi$.

---

### Conclusion

* **Closest point on $x + 2y + 2z = 4$ to $P = (3, 0, 0)$:** $Q = \left(\frac{28}{9}, \frac{2}{9}, \frac{2}{9}\right)$.
* **Shortest distance:** $d(P, \Pi) = \frac{1}{3}$.
* **Perpendicularity verification:** $\overrightarrow{PQ} = \left(\frac{1}{9}, \frac{2}{9}, \frac{2}{9}\right) = \frac{1}{9} n$ is a scalar multiple of the normal vector $n = (1, 2, 2)$, confirming that the segment $\overline{PQ}$ is perpendicular to the plane.
