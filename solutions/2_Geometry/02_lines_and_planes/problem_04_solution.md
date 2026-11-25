# Exercise 4. Plane Through Three Points

## Question

Find the equation of the plane through

$$
A = (1, 0, 0), \qquad B = (0, 1, 0), \qquad C = (0, 0, 1).
$$

First construct two vectors lying in the plane, and then use the cross product. Check the resulting equation on all three points.

---

## Solution

Three non-collinear points $A, B, C \in \mathbb{R}^3$ uniquely determine a plane. To construct its equation, we build two linearly independent vectors lying in the plane, compute a **normal vector** $n = \overrightarrow{AB} \times \overrightarrow{AC}$, and apply the point-normal formula $n \cdot (X - A) = 0$.

---

### 1. Construct Two Vectors Lying in the Plane

Using $A = (1, 0, 0)$ as the initial point, subtract its coordinates from $B = (0, 1, 0)$ and $C = (0, 0, 1)$:

$$
\overrightarrow{AB} = B - A = (0 - 1, \, 1 - 0, \, 0 - 0) = (-1, 1, 0)
$$

$$
\overrightarrow{AC} = C - A = (0 - 1, \, 0 - 0, \, 1 - 0) = (-1, 0, 1)
$$

Since $\overrightarrow{AC}$ is not a scalar multiple of $\overrightarrow{AB}$, these two vectors are linearly independent and span the plane's direction.

---

### 2. Compute a Normal Vector via the Cross Product

Apply the component-wise cross product formula $u \times v = (u_2 v_3 - u_3 v_2, \; u_3 v_1 - u_1 v_3, \; u_1 v_2 - u_2 v_1)$ with $u = \overrightarrow{AB} = (-1, 1, 0)$ and $v = \overrightarrow{AC} = (-1, 0, 1)$:

* **First component:** $(1)(1) - (0)(0) = 1 - 0 = 1$
* **Second component:** $(0)(-1) - (-1)(1) = 0 - (-1) = 1$
* **Third component:** $(-1)(0) - (1)(-1) = 0 - (-1) = 1$

Thus, a normal vector perpendicular to the plane is:

$$
n = \overrightarrow{AB} \times \overrightarrow{AC} = (1, 1, 1)
$$

* **Orthogonality check:** $n \cdot \overrightarrow{AB} = (1)(-1) + (1)(1) + (1)(0) = 0$ and $n \cdot \overrightarrow{AC} = (1)(-1) + (1)(0) + (1)(1) = 0$.

---

### 3. Write the Equation of the Plane

Substitute $A = (1, 0, 0)$ and $n = (1, 1, 1)$ into the point-normal equation $n \cdot (X - A) = 0$:

$$
1(x - 1) + 1(y - 0) + 1(z - 0) = 0
$$

Simplify to obtain the general equation of the plane:

$$
x - 1 + y + z = 0 \implies x + y + z = 1 \qquad (\text{or } x + y + z - 1 = 0)
$$

---

### 4. Check the Resulting Equation on All Three Points

Substitute each given point into $x + y + z = 1$:

* **For $A = (1, 0, 0)$:**

$$
1 + 0 + 0 = 1 \quad \checkmark
$$

* **For $B = (0, 1, 0)$:**

$$
0 + 1 + 0 = 1 \quad \checkmark
$$

* **For $C = (0, 0, 1)$:**

$$
0 + 0 + 1 = 1 \quad \checkmark
$$

All three points satisfy $x + y + z = 1$.

---

### Conclusion

* **Two in-plane vectors:** $\overrightarrow{AB} = (-1, 1, 0)$ and $\overrightarrow{AC} = (-1, 0, 1)$.
* **Normal vector:** $n = \overrightarrow{AB} \times \overrightarrow{AC} = (1, 1, 1)$.
* **Plane equation:** $x + y + z = 1$ (equivalently, $x + y + z - 1 = 0$).
* **Verification:** $A = (1, 0, 0)$, $B = (0, 1, 0)$, and $C = (0, 0, 1)$ each sum to $1$, confirming all three lie on the plane.
