# Exercise 9. Cross Product as a Perpendicular Direction

## Question

For $u = (1, 2, 0)$ and $v = (0, 1, 3)$ compute $u \times v$. Use dot products to check perpendicularity to both vectors, compute $v \times u$, and compare the results.

---

## Solution

In $\mathbb{R}^3$, the **cross product** (vector product) of two vectors $u = (u_1, u_2, u_3)$ and $v = (v_1, v_2, v_3)$ produces a vector orthogonal to both $u$ and $v$, defined component-wise by:

$$
u \times v = (u_2 v_3 - u_3 v_2, \; u_3 v_1 - u_1 v_3, \; u_1 v_2 - u_2 v_1)
$$

---

### 1. Compute $u \times v$

Substitute $u = (1, 2, 0)$ and $v = (0, 1, 3)$ into the cross product formula:

* **First component:** $(2)(3) - (0)(1) = 6 - 0 = 6$
* **Second component:** $(0)(0) - (1)(3) = 0 - 3 = -3$
* **Third component:** $(1)(1) - (2)(0) = 1 - 0 = 1$

Thus:

$$
u \times v = (6, -3, 1)
$$

---

### 2. Check Perpendicularity to Both $u$ and $v$ Using Dot Products

Two nonzero vectors in $\mathbb{R}^3$ are perpendicular if and only if their dot product equals $0$:

* **Check against $u = (1, 2, 0)$:**

$$
(u \times v) \cdot u = (6)(1) + (-3)(2) + (1)(0) = 6 - 6 + 0 = 0
$$

* **Check against $v = (0, 1, 3)$:**

$$
(u \times v) \cdot v = (6)(0) + (-3)(1) + (1)(3) = 0 - 3 + 3 = 0
$$

Since both dot products equal $0$, $u \times v = (6, -3, 1)$ is confirmed to be **perpendicular** to both $u$ and $v$.

---

### 3. Compute $v \times u$

Swap the order of the vectors so that $v = (0, 1, 3)$ is first and $u = (1, 2, 0)$ is second:

* **First component:** $(1)(0) - (3)(2) = 0 - 6 = -6$
* **Second component:** $(3)(1) - (0)(0) = 3 - 0 = 3$
* **Third component:** $(0)(2) - (1)(1) = 0 - 1 = -1$

Thus:

$$
v \times u = (-6, 3, -1)
$$

---

### 4. Compare $u \times v$ and $v \times u$ & Geometric Interpretation

* **Algebraic Comparison (Anticommutativity):** Comparing $u \times v = (6, -3, 1)$ and $v \times u = (-6, 3, -1)$ shows that reversing the order of multiplication negates every component:

$$
v \times u = -(u \times v)
$$

* **Geometric Interpretation (Right-Hand Rule & Area):**
  * **Magnitude:** Both vectors have the exact same length, $\|u \times v\| = \|v \times u\| = \sqrt{6^2 + (-3)^2 + 1^2} = \sqrt{46}$, which equals the area of the parallelogram spanned by $u$ and $v$.
  * **Orientation:** Both vectors lie along the same normal line perpendicular to the plane spanned by $u$ and $v$, but point in **opposite orientations** in accordance with the right-hand rule (curling fingers from $u$ to $v$ points along $u \times v$, whereas curling from $v$ to $u$ points in the exact opposite direction $-u \times v$).

---

### Conclusion

* **Cross product $u \times v$:** $(6, -3, 1)$.
* **Perpendicularity verification:** $(u \times v) \cdot u = 0$ and $(u \times v) \cdot v = 0$.
* **Reversed cross product and comparison:** $v \times u = (-6, 3, -1) = -(u \times v)$, demonstrating anticommutativity—same magnitude ($\sqrt{46}$) and normal line, opposite orientation.
