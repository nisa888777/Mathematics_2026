# Exercise 12. A Normal Vector to a Plane

## Question

Given $A = (1, 0, 2)$, $B = (2, 1, 0)$, and $C = (0, 3, 1)$. Construct two vectors lying in the plane, find a vector perpendicular to both, and check the perpendicularity using dot products.

---

## Solution

Three non-collinear points $A, B, C \in \mathbb{R}^3$ uniquely determine a plane. To find a **normal vector** $n$ perpendicular to this plane, we construct two non-parallel displacement vectors lying in the plane and compute their **cross product**:

$$
n = \overrightarrow{AB} \times \overrightarrow{AC}
$$

---

### 1. Construct Two Vectors Lying in the Plane

Using $A = (1, 0, 2)$ as the common initial point, subtract its coordinates from $B = (2, 1, 0)$ and $C = (0, 3, 1)$:

$$
\overrightarrow{AB} = B - A = (2 - 1, \, 1 - 0, \, 0 - 2) = (1, 1, -2)
$$

$$
\overrightarrow{AC} = C - A = (0 - 1, \, 3 - 0, \, 1 - 2) = (-1, 3, -1)
$$

Since $\overrightarrow{AC}$ is not a scalar multiple of $\overrightarrow{AB}$, these two vectors are linearly independent and span the direction of the plane.

---

### 2. Find a Vector Perpendicular to Both ($\overrightarrow{AB} \times \overrightarrow{AC}$)

Apply the component-wise cross product formula $u \times v = (u_2 v_3 - u_3 v_2, \; u_3 v_1 - u_1 v_3, \; u_1 v_2 - u_2 v_1)$ with $u = \overrightarrow{AB} = (1, 1, -2)$ and $v = \overrightarrow{AC} = (-1, 3, -1)$:

* **First component:** $(1)(-1) - (-2)(3) = -1 - (-6) = -1 + 6 = 5$
* **Second component:** $(-2)(-1) - (1)(-1) = 2 - (-1) = 2 + 1 = 3$
* **Third component:** $(1)(3) - (1)(-1) = 3 - (-1) = 3 + 1 = 4$

Thus, a normal vector perpendicular to the plane is:

$$
n = \overrightarrow{AB} \times \overrightarrow{AC} = (5, 3, 4)
$$

---

### 3. Check Perpendicularity Using Dot Products

Two nonzero vectors in $\mathbb{R}^3$ are perpendicular if and only if their Euclidean dot product equals $0$:

* **Check against $\overrightarrow{AB} = (1, 1, -2)$:**

$$
n \cdot \overrightarrow{AB} = (5)(1) + (3)(1) + (4)(-2) = 5 + 3 - 8 = 0
$$

* **Check against $\overrightarrow{AC} = (-1, 3, -1)$:**

$$
n \cdot \overrightarrow{AC} = (5)(-1) + (3)(3) + (4)(-1) = -5 + 9 - 4 = 0
$$

Since both dot products equal $0$, $n = (5, 3, 4)$ is confirmed to be **perpendicular** to both in-plane vectors (and therefore perpendicular to every vector lying in the plane, defining the plane equation $5(x - 1) + 3(y - 0) + 4(z - 2) = 0$, or $5x + 3y + 4z = 13$).

---

### Conclusion

* **Two vectors in the plane:** $\overrightarrow{AB} = (1, 1, -2)$ and $\overrightarrow{AC} = (-1, 3, -1)$.
* **Normal vector perpendicular to both:** $n = \overrightarrow{AB} \times \overrightarrow{AC} = (5, 3, 4)$.
* **Dot product verification:** $n \cdot \overrightarrow{AB} = 5 + 3 - 8 = 0$ and $n \cdot \overrightarrow{AC} = -5 + 9 - 4 = 0$.
