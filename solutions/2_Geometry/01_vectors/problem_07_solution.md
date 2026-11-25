# Exercise 7. Linear Dependence Without Heavy Computation

## Question

Given

$$
u = (1, 2, 3), \qquad v = (2, 4, 6), \qquad w = (0, 1, 1).
$$

Identify a specific relation between $u$ and $v$, decide whether the three vectors can be linearly independent, and explain why no long calculation is needed.

---

## Solution

To test linear dependence, we use the **Definition of Linear Dependence** and the **Subset Dependence Principle**:

* **Definition of Linear Dependence:** Vectors $u, v, w \in \mathbb{R}^3$ are **linearly dependent** if there exist scalars $c_1, c_2, c_3 \in \mathbb{R}$, **not all zero**, such that

$$
c_1 u + c_2 v + c_3 w = (0, 0, 0).
$$

* **Subset Dependence Principle:** If any subset of a set of vectors is already linearly dependent (for example, one vector is a scalar multiple of another), then the **entire set** of vectors is automatically linearly dependent.

---

### 1. Identify the Specific Relation Between $u$ and $v$

Comparing the components of $u = (1, 2, 3)$ and $v = (2, 4, 6)$, every coordinate of $v$ is exactly twice the corresponding coordinate of $u$:

$$
v = (2, 4, 6) = 2(1, 2, 3) = 2u
$$

Thus, $v$ is a **scalar multiple** of $u$ ($v = 2u$, or equivalently $2u - v = (0, 0, 0)$).

---

### 2. Decide Whether the Three Vectors Can Be Linearly Independent

Because $v = 2u$, the three vectors $u, v, w$ **cannot be linearly independent**; they are **linearly dependent**.

* **Explicit Nontrivial Combination (Verification):** Using $2u - v = (0, 0, 0)$ and setting the coefficient of $w$ to $0$ gives a linear combination equal to the zero vector with coefficients $(c_1, c_2, c_3) = (2, -1, 0) \neq (0, 0, 0)$:

$$
2u - 1v + 0w = 2(1, 2, 3) - (2, 4, 6) + 0(0, 1, 1) = (2 - 2 + 0, \, 4 - 4 + 0, \, 6 - 6 + 0) = (0, 0, 0)
$$

Since not all scalars are zero ($c_1 = 2 \neq 0$ and $c_2 = -1 \neq 0$), the set $\{u, v, w\}$ fails the definition of linear independence.

---

### 3. Why No Long Calculation Is Needed & Geometric Interpretation

* **Why no heavy computation is needed:** Standard procedures such as Gaussian elimination (row-reducing a $3 \times 3$ matrix) or computing a $3 \times 3$ determinant ($\det([u \; v \; w]) = 0$) are unnecessary because linear independence is a property of the *entire* set. Once two vectors in the set satisfy a nontrivial dependence relation ($2u - v = 0$), attaching any third vector $w$ with coefficient $c_3 = 0$ immediately produces a valid nontrivial dependence relation for all three vectors.
* **Geometric interpretation:** Because $v = 2u$, the vectors $u$ and $v$ are **collinear**—they lie on the exact same line through the origin in $\mathbb{R}^3$. Together with $w = (0, 1, 1)$, all three vectors lie within a single plane (or lower-dimensional subspace) passing through the origin rather than spanning all of $\mathbb{R}^3$, so the parallelepiped they form collapses to zero volume.

---

### Conclusion

* **Relation between $u$ and $v$:** $v = 2u$ ($v$ is a scalar multiple of $u$).
* **Linear independence decision:** The set $\{u, v, w\}$ **cannot be linearly independent** (it is **linearly dependent**), verified by $2u - v + 0w = (0, 0, 0)$.
* **Reason no long calculation is needed:** Because the subset $\{u, v\}$ is already linearly dependent, including $w$ with a zero coefficient immediately establishes linear dependence for the whole set without determinants or row reduction.
