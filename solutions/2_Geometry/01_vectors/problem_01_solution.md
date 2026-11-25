# Exercise 1. Vector Operations and Their Meaning

## Question

For $u = (2, -1, 3)$ and $v = (-1, 4, 2)$ compute

$$
u + v, \qquad u - v, \qquad 3u - 2v.
$$

Then verify that $(u + v) - v = u$, and explain geometrically what adding two vectors means.

---

## Solution

In $\mathbb{R}^3$, vector addition, subtraction, and scalar multiplication are performed **component-wise**: for $u = (u_1, u_2, u_3)$, $v = (v_1, v_2, v_3)$, and scalars $c, d \in \mathbb{R}$,

$$
cu + dv = (cu_1 + dv_1, \, cu_2 + dv_2, \, cu_3 + dv_3).
$$

---

### 1. Compute $u + v$, $u - v$, and $3u - 2v$

* **Vector addition ($u + v$):** Add corresponding components of $u$ and $v$:

$$
u + v = (2 + (-1), \, -1 + 4, \, 3 + 2) = (1, 3, 5)
$$

* **Vector subtraction ($u - v$):** Subtract each component of $v$ from the corresponding component of $u$:

$$
u - v = (2 - (-1), \, -1 - 4, \, 3 - 2) = (3, -5, 1)
$$

* **Linear combination ($3u - 2v$):** First apply scalar multiplication to each vector ($3u$ and $2v$), then subtract component-wise:

$$
3u = 3(2, -1, 3) = (6, -3, 9), \qquad 2v = 2(-1, 4, 2) = (-2, 8, 4)
$$

$$
3u - 2v = (6 - (-2), \, -3 - 8, \, 9 - 4) = (8, -11, 5)
$$

---

### 2. Verification of $(u + v) - v = u$

Using the computed result $u + v = (1, 3, 5)$ and subtracting $v = (-1, 4, 2)$ component-wise:

$$
(u + v) - v = (1, 3, 5) - (-1, 4, 2) = (1 - (-1), \, 3 - 4, \, 5 - 2) = (2, -1, 3) = u
$$

This confirms $(u + v) - v = u$, demonstrating that subtracting $v$ reverses the displacement added by $v$.

---

### 3. Geometric Meaning of Adding Two Vectors

Geometrically in $\mathbb{R}^3$, a vector represents a directed displacement (magnitude and direction). Adding two vectors $u$ and $v$ represents the **net combined displacement** obtained by applying one displacement after the other:

* **Tip-to-Tail (Triangle) Rule:** Place the tail (initial point) of $v$ at the tip (terminal point) of $u$. The sum vector $u + v$ is the directed arrow starting from the tail of $u$ and ending at the tip of $v$.
* **Parallelogram Rule:** When $u$ and $v$ are placed with their tails at the same starting point (such as the origin), they form two adjacent sides of a parallelogram, and $u + v$ is the **main diagonal** starting from that common tail.

---

### Conclusion

* **Computed vectors:** $u + v = (1, 3, 5)$, $u - v = (3, -5, 1)$, and $3u - 2v = (8, -11, 5)$.
* **Verification:** $(u + v) - v = (1, 3, 5) - (-1, 4, 2) = (2, -1, 3) = u$.
* **Geometric meaning:** Vector addition $u + v$ represents the resultant displacement formed either by placing $v$ tip-to-tail after $u$ or as the diagonal of the parallelogram spanned by $u$ and $v$.
