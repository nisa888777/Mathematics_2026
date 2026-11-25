# Exercise 13. Do Four Points Lie in One Plane?

## Question

Given

$$
A = (0, 0, 0), \qquad B = (1, 2, 0), \qquad C = (0, 1, 1), \qquad D = (2, 5, 1).
$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n = \overrightarrow{AB} \times \overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD} \cdot n = 0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A, B, C$, and justify the criterion.

---

## Solution

To test whether four points $A, B, C, D \in \mathbb{R}^3$ are **coplanar** (lie in a single plane), we combine the **cross product** and the **dot product** (the scalar triple product criterion $\overrightarrow{AD} \cdot (\overrightarrow{AB} \times \overrightarrow{AC}) = 0$)[span_2](start_span)[span_2](end_span):

* First, construct a normal vector $n = \overrightarrow{AB} \times \overrightarrow{AC}$ perpendicular to the plane spanned by $A, B, C$[span_3](start_span)[span_3](end_span).
* Second, test whether the displacement vector $\overrightarrow{AD}$ is orthogonal to $n$ via $\overrightarrow{AD} \cdot n = 0$[span_4](start_span)[span_4](end_span).

---

### 1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$

Subtract the coordinates of $A = (0, 0, 0)$ from $B = (1, 2, 0)$ and $C = (0, 1, 1)$[span_5](start_span)[span_5](end_span):

$$
\overrightarrow{AB} = B - A = (1 - 0, \, 2 - 0, \, 0 - 0) = (1, 2, 0)
$$

$$
\overrightarrow{AC} = C - A = (0 - 0, \, 1 - 0, \, 1 - 0) = (0, 1, 1)
$$

Since $\overrightarrow{AB}$ and $\overrightarrow{AC}$ are not scalar multiples of one another, $A, B, C$ are non-collinear and uniquely determine a plane[span_6](start_span)[span_6](end_span).

---

### 2. Find $n = \overrightarrow{AB} \times \overrightarrow{AC}$

Apply the component-wise cross product formula $u \times v = (u_2 v_3 - u_3 v_2, \; u_3 v_1 - u_1 v_3, \; u_1 v_2 - u_2 v_1)$ with $u = \overrightarrow{AB} = (1, 2, 0)$ and $v = \overrightarrow{AC} = (0, 1, 1)$[span_7](start_span)[span_7](end_span):

* **First component:** $(2)(1) - (0)(1) = 2 - 0 = 2$
* **Second component:** $(0)(0) - (1)(1) = 0 - 1 = -1$
* **Third component:** $(1)(1) - (2)(0) = 1 - 0 = 1$

Thus, the normal vector to the plane through $A, B, C$ is:

$$
n = \overrightarrow{AB} \times \overrightarrow{AC} = (2, -1, 1)
$$

* **Orthogonality verification:** $n \cdot \overrightarrow{AB} = (2)(1) + (-1)(2) + (1)(0) = 2 - 2 + 0 = 0$ and $n \cdot \overrightarrow{AC} = (2)(0) + (-1)(1) + (1)(1) = 0 - 1 + 1 = 0$.

---

### 3. Construct $\overrightarrow{AD}$ and Check Whether $\overrightarrow{AD} \cdot n = 0$

* **Step 1 — Construct $\overrightarrow{AD}$:** Subtract $A = (0, 0, 0)$ from $D = (2, 5, 1)$[span_8](start_span)[span_8](end_span):

$$
\overrightarrow{AD} = D - A = (2 - 0, \, 5 - 0, \, 1 - 0) = (2, 5, 1)
$$

* **Step 2 — Compute the dot product $\overrightarrow{AD} \cdot n$:**

$$
\overrightarrow{AD} \cdot n = (2)(2) + (5)(-1) + (1)(1) = 4 - 5 + 1 = 0
$$

Therefore, $\overrightarrow{AD} \cdot n = 0$ **holds**[span_9](start_span)[span_9](end_span).

---

### 4. Decision and Justification of the Coplanarity Criterion

* **Decision:** Yes, point $D = (2, 5, 1)$ **lies in the plane** determined by $A, B, C$ (so all four points $A, B, C, D$ are coplanar)[span_10](start_span)[span_10](end_span).
* **Justification of the Criterion:**
  * **Normal-Line Orthogonality:** The cross product $n = \overrightarrow{AB} \times \overrightarrow{AC} = (2, -1, 1)$ is perpendicular to the plane spanned by $\overrightarrow{AB}$ and $\overrightarrow{AC}$ starting at $A$. Every point $P$ in that plane satisfies the plane equation $n \cdot \overrightarrow{AP} = 0$ (here $2x - y + z = 0$). Because $\overrightarrow{AD} \cdot n = 0$, the vector $\overrightarrow{AD}$ has zero component along the normal direction $n$ and therefore lies entirely within the plane through $A$[span_11](start_span)[span_11](end_span).
  * **Zero Parallelepiped Volume & Linear Combination Check:** Equivalently, $|\overrightarrow{AD} \cdot (\overrightarrow{AB} \times \overrightarrow{AC})| = 0$ means the parallelepiped spanned by $\overrightarrow{AB}, \overrightarrow{AC}, \overrightarrow{AD}$ has zero volume, so $\overrightarrow{AD}$ is a linear combination of $\overrightarrow{AB}$ and $\overrightarrow{AC}$:

$$
2\overrightarrow{AB} + 1\overrightarrow{AC} = 2(1, 2, 0) + (0, 1, 1) = (2, 4, 0) + (0, 1, 1) = (2, 5, 1) = \overrightarrow{AD}
$$

---

### Conclusion

* **In-plane vectors:** $\overrightarrow{AB} = (1, 2, 0)$ and $\overrightarrow{AC} = (0, 1, 1)$[span_12](start_span)[span_12](end_span).
* **Normal vector:** $n = \overrightarrow{AB} \times \overrightarrow{AC} = (2, -1, 1)$[span_13](start_span)[span_13](end_span).
* **Test vector and dot product:** $\overrightarrow{AD} = (2, 5, 1)$ satisfies $\overrightarrow{AD} \cdot n = 4 - 5 + 1 = 0$[span_14](start_span)[span_14](end_span).
* **Coplanarity result:** $D$ **does lie** in the plane determined by $A, B, C$ ($2x - y + z = 0$), because $\overrightarrow{AD} \cdot n = 0$ guarantees that $\overrightarrow{AD}$ has zero projection onto the plane's normal direction and lies completely inside the plane ($\overrightarrow{AD} = 2\overrightarrow{AB} + \overrightarrow{AC}$)[span_15](start_span)[span_15](end_span).
