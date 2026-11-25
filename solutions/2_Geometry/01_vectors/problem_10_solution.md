# Exercise 10. Triangle Area from Vectors

## Question

The points $A = (0, 0, 0)$, $B = (2, 1, 0)$, and $C = (1, 3, 2)$ form a triangle. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$, compute the area of the parallelogram using the cross product, and then find the area of the triangle. Explain the factor $\frac{1}{2}$.

---

## Solution

In $\mathbb{R}^3$, two edge vectors emanating from a common vertex $A$ determine both a parallelogram and a triangle. Using the **cross product magnitude formula**, the area of the parallelogram spanned by $u = \overrightarrow{AB}$ and $v = \overrightarrow{AC}$ is:

$$
\text{Area}_{\text{parallelogram}} = \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \|\overrightarrow{AB}\|\|\overrightarrow{AC}\|\sin\theta
$$

---

### 1. Construct the Edge Vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$

Subtract the coordinates of the initial point $A = (0, 0, 0)$ from the terminal points $B = (2, 1, 0)$ and $C = (1, 3, 2)$:

$$
\overrightarrow{AB} = B - A = (2 - 0, \, 1 - 0, \, 0 - 0) = (2, 1, 0)
$$

$$
\overrightarrow{AC} = C - A = (1 - 0, \, 3 - 0, \, 2 - 0) = (1, 3, 2)
$$

---

### 2. Compute the Area of the Parallelogram Using the Cross Product

* **Step 1 — Compute the cross product $\overrightarrow{AB} \times \overrightarrow{AC}$:** Using $u = (2, 1, 0)$ and $v = (1, 3, 2)$ in $u \times v = (u_2 v_3 - u_3 v_2, \; u_3 v_1 - u_1 v_3, \; u_1 v_2 - u_2 v_1)$:
  * **First component:** $(1)(2) - (0)(3) = 2 - 0 = 2$
  * **Second component:** $(0)(1) - (2)(2) = 0 - 4 = -4$
  * **Third component:** $(2)(3) - (1)(1) = 6 - 1 = 5$

$$
\overrightarrow{AB} \times \overrightarrow{AC} = (2, -4, 5)
$$

*(Orthogonality check: $(2, -4, 5) \cdot (2, 1, 0) = 4 - 4 + 0 = 0$ and $(2, -4, 5) \cdot (1, 3, 2) = 2 - 12 + 10 = 0$.)*

* **Step 2 — Compute the Euclidean norm $\|\overrightarrow{AB} \times \overrightarrow{AC}\|$:**

$$
\text{Area}_{\text{parallelogram}} = \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \sqrt{2^2 + (-4)^2 + 5^2} = \sqrt{4 + 16 + 25} = \sqrt{45} = 3\sqrt{5}
$$

---

### 3. Find the Area of Triangle $\triangle ABC$

Taking half of the parallelogram area gives the area of $\triangle ABC$:

$$
\text{Area}_{\triangle ABC} = \frac{1}{2} \|\overrightarrow{AB} \times \overrightarrow{AC}\| = \frac{1}{2}\sqrt{45} = \frac{3\sqrt{5}}{2}
$$

---

### 4. Geometric Explanation of the Factor $\frac{1}{2}$

* **Diagonal Bisection of a Parallelogram:** Placing $\overrightarrow{AB}$ and $\overrightarrow{AC}$ tail-to-tail at vertex $A$ spans a parallelogram with vertices $A$, $B$, $D = A + \overrightarrow{AB} + \overrightarrow{AC} = (3, 4, 2)$, and $C$. The line segment $BC$ acts as a **diagonal** of this parallelogram, dividing it into two congruent triangles ($\triangle ABC \cong \triangle DCB$) with identical side lengths and equal areas.
* **Base-Times-Height Correspondence:** Equivalently, taking $\|\overrightarrow{AB}\|$ as the base and $\|\overrightarrow{AC}\|\sin\theta$ as the perpendicular height $h$, the parallelogram has area $\text{base} \times \text{height} = \|\overrightarrow{AB} \times \overrightarrow{AC}\|$, whereas the triangle has area $\frac{1}{2} \times \text{base} \times \text{height} = \frac{1}{2}\|\overrightarrow{AB} \times \overrightarrow{AC}\|$.

---

### Conclusion

* **Constructed vectors:** $\overrightarrow{AB} = (2, 1, 0)$ and $\overrightarrow{AC} = (1, 3, 2)$.
* **Parallelogram area:** $\|\overrightarrow{AB} \times \overrightarrow{AC}\| = \|(2, -4, 5)\| = \sqrt{45} = 3\sqrt{5}$.
* **Triangle area:** $\text{Area}_{\triangle ABC} = \frac{1}{2}\sqrt{45} = \frac{3\sqrt{5}}{2}$, where the factor $\frac{1}{2}$ arises because the diagonal $BC$ bisects the spanned parallelogram into two congruent triangles of equal area.
