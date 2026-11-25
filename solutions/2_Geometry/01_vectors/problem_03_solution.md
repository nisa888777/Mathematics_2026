# Exercise 3. Vector Normalization

## Question

For $v = (3, 4)$ find a unit vector $e$ with the same direction and orientation. Check that $\|e\| = 1$, reconstruct $v$ in the form $v = \|v\|e$, and explain what changes during normalization and what remains unchanged.

---

## Solution

---

### 1. Find the Unit Vector $e$

* **Mechanism (Vector Normalization):** A nonzero vector $v$ is normalized into a unit vector $e$ pointing in the exact same direction and orientation by scaling $v$ by the reciprocal of its Euclidean norm $\|v\|$:

$$
e = \frac{1}{\|v\|} v = \frac{v}{\|v\|}
$$

* **Step 1 — Compute the length $\|v\|$:** Using the Euclidean norm in $\mathbb{R}^2$ for $v = (3, 4)$:

$$
\|v\| = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5
$$

* **Step 2 — Scale $v$ by $\frac{1}{\|v\|}$:**

$$
e = \frac{1}{5}(3, 4) = \left( \frac{3}{5}, \, \frac{4}{5} \right) = (0.6, \, 0.8)
$$

---

### 2. Check That $\|e\| = 1$

Applying the Euclidean norm formula to $e = \left( \frac{3}{5}, \, \frac{4}{5} \right)$:

$$
\|e\| = \sqrt{\left(\frac{3}{5}\right)^2 + \left(\frac{4}{5}\right)^2} = \sqrt{\frac{9}{25} + \frac{16}{25}} = \sqrt{\frac{25}{25}} = \sqrt{1} = 1
$$

This confirms that $e$ has unit length ($1$).

---

### 3. Reconstruct $v$ in the Form $v = \|v\|e$

Multiplying the unit vector $e = \left( \frac{3}{5}, \, \frac{4}{5} \right)$ by the scalar length $\|v\| = 5$:

$$
\|v\|e = 5 \left( \frac{3}{5}, \, \frac{4}{5} \right) = \left( 5 \cdot \frac{3}{5}, \, 5 \cdot \frac{4}{5} \right) = (3, 4) = v
$$

This demonstrates the polar/magnitude-direction decomposition $v = \|v\|e$, where $\|v\| = 5$ encodes the magnitude and $e = \left( \frac{3}{5}, \, \frac{4}{5} \right)$ encodes the pure direction.

---

### 4. What Changes and What Remains Unchanged During Normalization

* **What changes (Length / Magnitude):** The magnitude of the vector is rescaled from $\|v\| = 5$ down to $\|e\| = 1$. Geometrically, the vector is contracted along its ray so that its tip lies on the unit circle centered at the origin.
* **What remains unchanged (Direction and Orientation):** Because we multiply $v$ by a **strictly positive** scalar $\frac{1}{\|v\|} = \frac{1}{5} > 0$, the line of action (direction) and the sense along that line (orientation, i.e., the angle $\theta$ with the positive $x$-axis, where $\cos\theta = \frac{3}{5}$ and $\sin\theta = \frac{4}{5}$) are completely preserved.

---

### Conclusion

* **Unit vector:** $e = \left( \frac{3}{5}, \, \frac{4}{5} \right)$.
* **Verification and reconstruction:** $\|e\| = 1$ and $v = 5 \left( \frac{3}{5}, \, \frac{4}{5} \right) = (3, 4)$.
* **Geometric effect:** Normalization rescales the vector's length to $1$ while leaving its direction and orientation unchanged.
