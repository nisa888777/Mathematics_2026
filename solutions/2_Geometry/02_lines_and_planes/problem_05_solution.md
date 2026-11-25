# Exercise 5. Relative Position of Two Lines

## Question

Analyze the position of

$$
L_1: (x, y, z) = (1, 1, 0) + t(1, 2, 1),
$$

$$
L_2: (x, y, z) = (2, 0, 1) + s(0, 1, -1).
$$

If they intersect, give the intersection point. If not, determine whether they are parallel or skew. Justify the classification.

---

## Solution

In $\mathbb{R}^3$, two distinct lines $L_1$ and $L_2$ have one of three possible relative positions:

1. **Parallel:** Their direction vectors are scalar multiples of each other.
2. **Intersecting:** Their direction vectors are non-parallel and the parametric equations share a common solution $t, s \in \mathbb{R}$.
3. **Skew:** Their direction vectors are non-parallel and the lines do not intersect, meaning they do not lie in a common plane.

---

### 1. Check Whether the Direction Vectors Are Parallel

Read the base points and direction vectors from the given parametric equations:

* **For $L_1$:** Base point $P_1 = (1, 1, 0)$ and direction vector $v_1 = (1, 2, 1)$.
* **For $L_2$:** Base point $P_2 = (2, 0, 1)$ and direction vector $v_2 = (0, 1, -1)$.

Test whether $v_1 = k v_2$ for any scalar $k \in \mathbb{R}$:

* Comparing the first components requires $1 = k(0) = 0$, which is impossible.

Thus, $v_1$ and $v_2$ are **not scalar multiples** of each other, so **$L_1$ and $L_2$ are not parallel**.

---

### 2. Test for an Intersection Point

Set the coordinate expressions of $L_1$ and $L_2$ equal to each other:

$$
(1 + t, \, 1 + 2t, \, t) = (2, \, s, \, 1 - s)
$$

This produces a linear system of three equations in two unknowns $t$ and $s$:

$$
\begin{cases}
1 + t = 2 & \text{(Equation 1: } x\text{-coordinate)} \\
1 + 2t = s & \text{(Equation 2: } y\text{-coordinate)} \\
t = 1 - s & \text{(Equation 3: } z\text{-coordinate)}
\end{cases}
$$

* **Step 1 — Solve Equations 1 and 2:**
  * From Equation 1: $1 + t = 2 \implies t = 1$.
  * Substitute $t = 1$ into Equation 2: $s = 1 + 2(1) = 3$.

* **Step 2 — Check Equation 3 for consistency:**
  * Substitute $t = 1$ and $s = 3$ into Equation 3 ($t = 1 - s$):

$$
\text{LHS} = 1, \qquad \text{RHS} = 1 - 3 = -2
$$

Since $1 \neq -2$, the system is **inconsistent** and has **no solution** $t, s \in \mathbb{R}$. Therefore, **$L_1$ and $L_2$ do not intersect**.

---

### 3. Classify and Justify the Relative Position

* **Classification:** $L_1$ and $L_2$ are **skew lines**.
* **Justification:**
  1. **Non-parallel directions:** $v_1 = (1, 2, 1)$ and $v_2 = (0, 1, -1)$ are linearly independent with $v_1 \times v_2 = (-3, 1, 1) \neq (0, 0, 0)$, ruling out parallel or coincident lines.
  2. **Empty intersection:** The coordinate system yields a unique candidate $t = 1, \; s = 3$ from the $x$- and $y$-equations that fails the $z$-equation ($1 \neq -2$), proving $L_1 \cap L_2 = \varnothing$.
  3. **Non-coplanarity (Scalar Triple Product Check):** Using $\overrightarrow{P_1 P_2} = P_2 - P_1 = (1, -1, 1)$ and $v_1 \times v_2 = (-3, 1, 1)$, the scalar triple product is:

$$
\overrightarrow{P_1 P_2} \cdot (v_1 \times v_2) = (1)(-3) + (-1)(1) + (1)(1) = -3 - 1 + 1 = -3 \neq 0
$$

Because this determinant is nonzero, $L_1$ and $L_2$ do not lie in any single plane, which is the defining geometric property of **skew lines** in $\mathbb{R}^3$.

---

### Conclusion

* **Parallel check:** $v_1 = (1, 2, 1)$ and $v_2 = (0, 1, -1)$ are not scalar multiples, so the lines are **not parallel**.
* **Intersection check:** Solving the $x$- and $y$-equations gives $t = 1$ and $s = 3$, which contradicts the $z$-equation ($1 \neq 1 - 3 = -2$), so the lines **do not intersect**.
* **Final classification:** $L_1$ and $L_2$ are **skew lines** (non-parallel, non-intersecting, and non-coplanar with $\overrightarrow{P_1 P_2} \cdot (v_1 \times v_2) = -3 \neq 0$).
