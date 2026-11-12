# Exercise 8. Inverse of a Transformation

## Question

The matrix

$$
S = \begin{pmatrix} 2 & 0 \\\ 0 & \frac{1}{2} \end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S, S^{-1}$ on one simple vector.

---

## Solution

We are given the $2 \times 2$ diagonal scaling matrix:

$$
S = \begin{pmatrix} 2 & 0 \\\ 0 & \frac{1}{2} \end{pmatrix}
$$

---

### 1. Compute $S^{-1}$

First, we find the determinant of $S$:

$$
\det(S) = (2)\left(\frac{1}{2}\right) - (0)(0) = 1
$$

Since $\det(S) = 1 \neq 0$, $S^{-1}$ exists. Applying the $2 \times 2$ inverse formula:

$$
S^{-1} = \frac{1}{1} \begin{pmatrix} \frac{1}{2} & 0 \\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\\ 0 & 2 \end{pmatrix}
$$

*(Note: For any invertible diagonal matrix, the inverse is obtained directly by taking the reciprocal of each non-zero diagonal entry.)*

---

### 2. Geometric Interpretation of $S^{-1}$

* **Action of $S$:** Scales the plane horizontally ($x$-direction) by a factor of $2$ (stretching by $2$) and vertically ($y$-direction) by a factor of $\frac{1}{2}$ (compressing by $2$).
* **Action of $S^{-1}$:** Undoes the scaling performed by $S$ by compressing the plane horizontally ($x$-direction) by a factor of $\frac{1}{2}$ and stretching it vertically ($y$-direction) by a factor of $2$.

---

### 3. Check the Action of $S$ and $S^{-1}$ on a Simple Vector

Let us choose the simple test vector:

$$
\mathbf{v} = \begin{pmatrix} 1 \\\ 4 \end{pmatrix}
$$

First, apply the transformation $S$ to $\mathbf{v}$:

$$
\mathbf{w} = S\mathbf{v} = \begin{pmatrix} 2 & 0 \\\ 0 & \frac{1}{2} \end{pmatrix} \begin{pmatrix} 1 \\\ 4 \end{pmatrix} = \begin{pmatrix} 2(1) + 0(4) \\\ 0(1) + \frac{1}{2}(4) \end{pmatrix} = \begin{pmatrix} 2 \\\ 2 \end{pmatrix}
$$

Next, apply the inverse transformation $S^{-1}$ to the resulting vector $\mathbf{w}$:

$$
S^{-1}\mathbf{w} = S^{-1}(S\mathbf{v}) = \begin{pmatrix} \frac{1}{2} & 0 \\\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 \\\ 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(2) + 0(2) \\\ 0(2) + 2(2) \end{pmatrix} = \begin{pmatrix} 1 \\\ 4 \end{pmatrix} = \mathbf{v}
$$

Applying $S$ followed by $S^{-1}$ returns the exact original vector $\mathbf{v}$, confirming that $S^{-1}$ geometrically reverses the transformation $S$.

---

### Conclusion

* The inverse transformation matrix is:

$$
S^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\\ 0 & 2 \end{pmatrix}
$$

* Geometrically, $S^{-1}$ shrinks the $x$-coordinate by half and doubles the $y$-coordinate, completely undoing the scaling performed by $S$ so that $S^{-1}(S\mathbf{v}) = \mathbf{v}$.
