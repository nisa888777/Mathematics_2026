# Exercise 2. Distance as the Length of a Vector

## Question

The points are $A = (1, 2, 3)$ and $B = (4, -2, 6)$.

1. Construct $\overrightarrow{AB}$.
2. Compute its length.
3. Compute the distance between the points using the coordinate formula.
4. Explain why both calculations give the same result.

---

## Solution

We treat points in $\mathbb{R}^3$ via their position vectors relative to the origin $O = (0, 0, 0)$, so $\overrightarrow{OA} = (1, 2, 3)$ and $\overrightarrow{OB} = (4, -2, 6)$.

---

### 1. Construct $\overrightarrow{AB}$

* **Mechanism (Displacement / Difference of Position Vectors):** The directed vector from initial point $A = (x_1, y_1, z_1)$ to terminal point $B = (x_2, y_2, z_2)$ is obtained by subtracting the coordinates of $A$ from the coordinates of $B$:

$$
\overrightarrow{AB} = \overrightarrow{OB} - \overrightarrow{OA} = (x_2 - x_1, \, y_2 - y_1, \, z_2 - z_1)
$$

* **Calculation:**

$$
\overrightarrow{AB} = (4 - 1, \, -2 - 2, \, 6 - 3) = (3, -4, 3)
$$

---

### 2. Compute the Length of $\overrightarrow{AB}$

* **Mechanism (Euclidean Norm in $\mathbb{R}^3$):** The length (magnitude or Euclidean norm) of a vector $v = (v_1, v_2, v_3)$ is defined by the square root of the sum of the squares of its components:

$$
\|v\| = \sqrt{v_1^2 + v_2^2 + v_3^2}
$$

* **Calculation:**

$$
\|\overrightarrow{AB}\| = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}
$$

---

### 3. Distance Between $A$ and $B$ Using the Coordinate Formula

* **Mechanism (3D Euclidean Distance Formula):** The straight-line distance $d(A, B)$ between two points $A = (x_1, y_1, z_1)$ and $B = (x_2, y_2, z_2)$ in $\mathbb{R}^3$ is given by:

$$
d(A, B) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}
$$

* **Calculation:**

$$
d(A, B) = \sqrt{(4 - 1)^2 + (-2 - 2)^2 + (6 - 3)^2} = \sqrt{3^2 + (-4)^2 + 3^2} = \sqrt{9 + 16 + 9} = \sqrt{34}
$$

---

### 4. Why Both Calculations Give the Same Result

* **Algebraic equivalence:** By definition, the components of the displacement vector $\overrightarrow{AB}$ are precisely the coordinate differences $\Delta x = x_2 - x_1$, $\Delta y = y_2 - y_1$, and $\Delta z = z_2 - z_1$. Consequently, applying the Euclidean norm formula $\|\overrightarrow{AB}\| = \sqrt{(\Delta x)^2 + (\Delta y)^2 + (\Delta z)^2}$ performs the exact same arithmetic operations as the 3D coordinate distance formula $d(A, B)$.
* **Geometric interpretation:** Shifting the vector $\overrightarrow{AB}$ so that its tail lies at the origin $(0, 0, 0)$ places its tip at $(3, -4, 3)$ without changing its length or direction. In $\mathbb{R}^3$, both calculations measure the length of the space diagonal of the same axis-aligned rectangular box with side lengths $|\Delta x| = 3$, $|\Delta y| = 4$, and $|\Delta z| = 3$ (a two-step application of the Pythagorean theorem).

---

### Conclusion

* **Displacement vector:** $\overrightarrow{AB} = (3, -4, 3)$.
* **Vector length and point distance:** $\|\overrightarrow{AB}\| = d(A, B) = \sqrt{34}$.
* **Equivalence:** The 3D distance formula between two points is simply the Euclidean norm of their difference vector $\overrightarrow{AB} = \overrightarrow{OB} - \overrightarrow{OA}$.
