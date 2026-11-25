# Exercise 14. Closest Point on a Line

## Question

Given a point $P = (4, 1)$ and a line through the origin with direction $v = (1, 2)$. Using projection, find the closest point on the line, the distance from $P$ to the line, and verify that the appropriate vector is perpendicular to the direction of the line.

---

## Solution

In $\mathbb{R}^2$, the line $L$ passing through the origin $O = (0, 0)$ with direction $v = (1, 2)$ consists of all scalar multiples $t v$ ($t \in \mathbb{R}$). Representing $P = (4, 1)$ by its position vector $p = \overrightarrow{OP} = (4, 1)$, the **closest point** $Q$ on $L$ to $P$ is given by the **orthogonal projection** of $p$ onto $v$:

$$
q = \overrightarrow{OQ} = \text{proj}_{v} p = \frac{p \cdot v}{v \cdot v} v
$$

---

### 1. Find the Closest Point $Q$ on the Line

* **Step 1 — Compute the dot products $p \cdot v$ and $v \cdot v$:**

$$
p \cdot v = (4)(1) + (1)(2) = 4 + 2 = 6
$$

$$
v \cdot v = \|v\|^2 = 1^2 + 2^2 = 1 + 4 = 5
$$

* **Step 2 — Scale $v$ to obtain $\text{proj}_{v} p$:**

$$
q = \text{proj}_{v} p = \frac{6}{5}(1, 2) = \left(\frac{6}{5}, \, \frac{12}{5}\right)
$$

Since the line passes through the origin $(0, 0)$, the closest point on the line is:

$$
Q = \left(\frac{6}{5}, \, \frac{12}{5}\right) = (1.2, \, 2.4)
$$

---

### 2. Find the Distance From $P$ to the Line

* **Step 1 — Construct the perpendicular error vector $\overrightarrow{QP} = p - q$:**

$$
\overrightarrow{QP} = p - \text{proj}_{v} p = (4, 1) - \left(\frac{6}{5}, \, \frac{12}{5}\right) = \left(\frac{20}{5} - \frac{6}{5}, \, \frac{5}{5} - \frac{12}{5}\right) = \left(\frac{14}{5}, \, -\frac{7}{5}\right)
$$

* **Step 2 — Compute the Euclidean norm $\|\overrightarrow{QP}\|$:**

$$
d(P, L) = \|\overrightarrow{QP}\| = \sqrt{\left(\frac{14}{5}\right)^2 + \left(-\frac{7}{5}\right)^2} = \sqrt{\frac{196}{25} + \frac{49}{25}} = \sqrt{\frac{245}{25}} = \frac{\sqrt{49 \cdot 5}}{5} = \frac{7\sqrt{5}}{5}
$$

---

### 3. Verify Perpendicularity to the Direction of the Line

To confirm that $Q$ minimizes the distance, the displacement vector $\overrightarrow{QP} = \left(\frac{14}{5}, \, -\frac{7}{5}\right)$ connecting the closest point $Q$ to $P$ must be orthogonal to the line's direction $v = (1, 2)$:

$$
\overrightarrow{QP} \cdot v = \left(\frac{14}{5}\right)(1) + \left(-\frac{7}{5}\right)(2) = \frac{14}{5} - \frac{14}{5} = 0
$$

* **Geometric Verification (Pythagorean Theorem):** Because $\overrightarrow{QP} \perp v$, for any other point $X$ on the line $L$, $\triangle PQX$ forms a right triangle with hypotenuse $PX$, so $\|PX\|^2 = \|PQ\|^2 + \|QX\|^2 > \|PQ\|^2$ whenever $X \neq Q$. Additionally, $\|p\|^2 = \|q\|^2 + \|\overrightarrow{QP}\|^2$ holds: $17 = \frac{180}{25} + \frac{245}{25} = \frac{425}{25} = 17$.

---

### Conclusion

* **Closest point on the line:** $Q = \left(\frac{6}{5}, \, \frac{12}{5}\right)$.
* **Distance from $P$ to the line:** $d(P, L) = \|\overrightarrow{QP}\| = \frac{7\sqrt{5}}{5}$.
* **Perpendicularity verification:** $\overrightarrow{QP} \cdot v = \left(\frac{14}{5}, \, -\frac{7}{5}\right) \cdot (1, 2) = \frac{14}{5} - \frac{14}{5} = 0$, confirming $\overrightarrow{QP} \perp v$.
