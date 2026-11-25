# Exercise 6. Angle Between Planes

## Question

Given

$$
\Pi_1: x + y + z = 1, \qquad \Pi_2: x - y = 2.
$$

First use the normal vectors to decide whether the planes are parallel. If not, compute the angle between them and explain why the normal vectors alone are enough for this calculation.

---

## Solution

In $\mathbb{R}^3$, a plane $ax + by + cz = d$ has normal vector $n = (a, b, c)$. Two planes are parallel if and only if their normal vectors are scalar multiples of each other, and the acute angle $\theta \in [0, \frac{\pi}{2}]$ between two intersecting planes equals the acute angle between their normal vectors:

$$
\cos\theta = \frac{|n_1 \cdot n_2|}{\|n_1\| \, \|n_2\|}
$$

---

### 1. Identify the Normal Vectors and Check for Parallelism

Read the coefficients of $x, y, z$ from each plane equation:

* **Normal vector to $\Pi_1$ ($x + y + z = 1$):**

$$
n_1 = (1, 1, 1)
$$

* **Normal vector to $\Pi_2$ ($x - y + 0z = 2$):**

$$
n_2 = (1, -1, 0)
$$

Test whether $n_1 = k n_2$ for any scalar $k \in \mathbb{R}$:

* Comparing the third components requires $1 = k(0) = 0$, which is impossible (and comparing the first two components gives $k = 1$ from $x$ versus $k = -1$ from $y$).

Because $n_1$ and $n_2$ are **not scalar multiples** of each other, **the planes $\Pi_1$ and $\Pi_2$ are not parallel** (they intersect along a line).

---

### 2. Compute the Angle Between the Planes

* **Step 1 — Compute the dot product $n_1 \cdot n_2$:**

$$
n_1 \cdot n_2 = (1)(1) + (1)(-1) + (1)(0) = 1 - 1 + 0 = 0
$$

* **Step 2 — Compute the Euclidean norms $\|n_1\|$ and $\|n_2\|$:**

$$
\|n_1\| = \sqrt{1^2 + 1^2 + 1^2} = \sqrt{3}, \qquad \|n_2\| = \sqrt{1^2 + (-1)^2 + 0^2} = \sqrt{2}
$$

* **Step 3 — Solve for the angle $\theta$:**

$$
\cos\theta = \frac{|n_1 \cdot n_2|}{\|n_1\| \, \|n_2\|} = \frac{0}{\sqrt{3}\sqrt{2}} = 0 \implies \theta = \arccos(0) = \frac{\pi}{2} = 90^\circ
$$

Thus, $\Pi_1$ and $\Pi_2$ intersect at a **$90^\circ$ ($\frac{\pi}{2}\text{ rad}$) angle**—that is, the two planes are **perpendicular (orthogonal)**.

---

### 3. Explain Why the Normal Vectors Alone Are Enough

1. **Unique Orientation Determination:** A normal vector $n_i$ completely determines the tilt (2D direction subspace) of a plane $\Pi_i$ in $\mathbb{R}^3$. Changing the right-hand side constant ($d_1 = 1$ or $d_2 = 2$) only translates the plane parallel to itself without altering its orientation or the dihedral angle at which it meets another plane.
2. **Rigid $90^\circ$ Rotation Invariance in the Cross-Sectional Plane:** Looking along the line of intersection of $\Pi_1$ and $\Pi_2$, the cross-section reduces to two lines in a 2D plane perpendicular to the intersection line. Rotating each plane's cross-sectional line by $90^\circ$ produces the directions of $n_1$ and $n_2$. Because a rigid rotation preserves angles between lines, the angle between $n_1$ and $n_2$ (up to choosing the acute supplement via $|n_1 \cdot n_2|$) is **identical** to the dihedral angle between $\Pi_1$ and $\Pi_2$.
3. **No Intersection Line Needed:** Because $n_1$ and $n_2$ already encode the full angular relationship between the two planes, we do not need to solve for their line of intersection or pick points on the planes to measure the angle.

---

### Conclusion

* **Normal vectors:** $n_1 = (1, 1, 1)$ and $n_2 = (1, -1, 0)$.
* **Parallelism check:** Since $n_1$ is not a scalar multiple of $n_2$, **$\Pi_1$ and $\Pi_2$ are not parallel**.
* **Angle between $\Pi_1$ and $\Pi_2$:** Because $n_1 \cdot n_2 = 0$, $\cos\theta = 0$, so the angle between the planes is **$\theta = 90^\circ$ ($\frac{\pi}{2}\text{ rad}$)**—the planes are perpendicular.
* **Why normals suffice:** Normal vectors completely capture each plane's spatial orientation independently of parallel shifts, and rotating two intersecting planes by $90^\circ$ into their normal directions preserves the angle between them.
