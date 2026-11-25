# Exercise 4. Dot Product and Perpendicularity

## Question

For $u = (1, 2, -1)$ and $v = (2, -1, 3)$ compute $u \cdot v$ and determine whether the vectors are perpendicular. Then find $a$ so that $w = (2, -1, a)$ is perpendicular to $u$, and check the result.

---

## Solution

In $\mathbb{R}^3$, we use the **Euclidean dot product** (scalar product) and the **orthogonality criterion**:

* **Dot Product Mechanism:** For $u = (u_1, u_2, u_3)$ and $v = (v_1, v_2, v_3)$,

$$
u \cdot v = u_1 v_1 + u_2 v_2 + u_3 v_3
$$

* **Perpendicularity (Orthogonality) Mechanism:** Two nonzero vectors $u$ and $v$ are perpendicular ($u \perp v$) if and only if their dot product equals zero ($u \cdot v = 0$), because $u \cdot v = \|u\|\|v\|\cos\theta$ and $\cos(90^\circ) = 0$.

---

### 1. Compute $u \cdot v$ and Test Perpendicularity

* **Calculation:**

$$
u \cdot v = (1)(2) + (2)(-1) + (-1)(3) = 2 - 2 - 3 = -3
$$

* **Perpendicularity Test:** Since $u \cdot v = -3 \neq 0$, the vectors $u$ and $v$ are **not perpendicular**. (Furthermore, because $u \cdot v < 0$, the angle $\theta$ between them is obtuse: $90^\circ < \theta \le 180^\circ$.)

---

### 2. Find $a$ So That $w = (2, -1, a)$ Is Perpendicular to $u$

Impose the orthogonality condition $u \cdot w = 0$:

$$
u \cdot w = (1)(2) + (2)(-1) + (-1)(a) = 0
$$

Simplify and solve for $a$:

$$
2 - 2 - a = 0 \implies -a = 0 \implies a = 0
$$

Thus, the required vector is $w = (2, -1, 0)$.

---

### 3. Check the Result and Geometric Interpretation

* **Verification:** Substitute $a = 0$ into $w = (2, -1, 0)$ and compute $u \cdot w$ directly:

$$
u \cdot w = (1)(2) + (2)(-1) + (-1)(0) = 2 - 2 + 0 = 0
$$

Since $u \cdot w = 0$, the vector $w = (2, -1, 0)$ is indeed perpendicular to $u = (1, 2, -1)$.

* **Geometric Interpretation:** All vectors $x = (x_1, x_2, x_3)$ satisfying $u \cdot x = x_1 + 2x_2 - x_3 = 0$ form a plane through the origin with normal vector $u = (1, 2, -1)$. Fixing the first two components to $(2, -1)$ specifies a vertical line in $\mathbb{R}^3$ that pierces this perpendicular plane at the unique height $z = a = 0$.

---

### Conclusion

* **Dot product and test:** $u \cdot v = -3 \neq 0$, so $u$ and $v$ are **not perpendicular**.
* **Parameter for perpendicularity:** $a = 0$, giving $w = (2, -1, 0)$, which satisfies $u \cdot w = 0$.
