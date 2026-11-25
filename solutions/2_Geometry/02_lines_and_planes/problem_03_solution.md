# Exercise 3. Plane Through a Point with a Given Normal Vector

## Question

Find the equation of the plane through $P = (1, -2, 3)$ and perpendicular to $n = (2, 1, -1)$. Check the result by substituting the point $P$ and explain the role of the normal vector.

---

## Solution

In $\mathbb{R}^3$, a plane passing through a point $P = (x_0, y_0, z_0)$ and perpendicular to a nonzero normal vector $n = (a, b, c)$ consists of all points $X = (x, y, z)$ such that the displacement vector $\overrightarrow{PX} = X - P$ is orthogonal to $n$:

$$
n \cdot \overrightarrow{PX} = 0 \iff a(x - x_0) + b(y - y_0) + c(z - z_0) = 0
$$

---

### 1. Construct the Equation of the Plane

Substitute $P = (1, -2, 3)$ and $n = (2, 1, -1)$ into the point-normal form:

$$
2(x - 1) + 1(y - (-2)) + (-1)(z - 3) = 0
$$

Simplify the signs and expand each term:

$$
2(x - 1) + (y + 2) - (z - 3) = 0
$$

$$
2x - 2 + y + 2 - z + 3 = 0
$$

Combine the constant terms ($-2 + 2 + 3 = 3$):

$$
2x + y - z + 3 = 0 \qquad \text{or} \qquad 2x + y - z = -3
$$

---

### 2. Check the Result by Substituting the Point $P$

Substitute $P = (1, -2, 3)$ into the left-hand side of $2x + y - z + 3 = 0$:

$$
2(1) + (-2) - (3) + 3 = 2 - 2 - 3 + 3 = 0
$$

Since $0 = 0$ holds identically, $P = (1, -2, 3)$ lies on the plane.

* **Additional In-Plane Vector Orthogonality Check:** Choosing another point satisfying $2x + y - z + 3 = 0$, such as $Q = (0, 0, 3)$ (since $2(0) + 0 - 3 + 3 = 0$), gives $\overrightarrow{PQ} = (-1, 2, 0)$. Taking the dot product confirms $n \cdot \overrightarrow{PQ} = (2)(-1) + (1)(2) + (-1)(0) = -2 + 2 + 0 = 0$.

---

### 3. Explain the Role of the Normal Vector

1. **Fixes the Orientation (Tilt) of the Plane:** The normal vector $n = (2, 1, -1)$ specifies the unique direction in $\mathbb{R}^3$ perpendicular to the plane. Any vector lying inside the plane must form a $90^\circ$ angle with $n$ ($n \cdot \overrightarrow{PX} = 0$).
2. **Directly Supplies the Coefficients of $x, y, z$:** Expanding $n \cdot (X - P) = 0$ produces $n \cdot X = n \cdot P$, so the components of $n = (2, 1, -1)$ appear directly as the coefficients $(2, 1, -1)$ of $x, y, z$ in $2x + y - z = -3$.
3. **Separates Orientation From Position:** Changing the constant term on the right-hand side shifts the plane parallel to itself without changing $n$, while the point $P = (1, -2, 3)$ locks in the exact constant $d = n \cdot P = (2)(1) + (1)(-2) + (-1)(3) = -3$.

---

### Conclusion

* **Point-normal equation:** $2(x - 1) + (y + 2) - (z - 3) = 0$.
* **General equation:** $2x + y - z + 3 = 0$ (equivalently, $2x + y - z = -3$).
* **Point substitution check:** $2(1) + (-2) - 3 + 3 = 0$, confirming $P = (1, -2, 3)$ lies on the plane.
* **Role of $n = (2, 1, -1)$:** Defines the plane's unique perpendicular orientation in $\mathbb{R}^3$ and directly determines the variable coefficients $(2, 1, -1)$ in the linear equation.
