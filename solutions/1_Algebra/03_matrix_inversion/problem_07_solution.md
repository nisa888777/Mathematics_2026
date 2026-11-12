# Exercise 7. Inverse of a Product

## Question

For

$$
A = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\\ 0 & 3 \end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

---

## Solution

We are given two $2 \times 2$ invertible matrices:

$$
A = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 2 & 0 \\\ 0 & 3 \end{pmatrix}
$$

---

### 1. Compute $(AB)^{-1}$

First, we compute the matrix product $AB$:

$$
AB = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\\ 0 & 3 \end{pmatrix} = \begin{pmatrix} (1)(2) + (1)(0) & (1)(0) + (1)(3) \\\ (0)(2) + (1)(0) & (0)(0) + (1)(3) \end{pmatrix} = \begin{pmatrix} 2 & 3 \\\ 0 & 3 \end{pmatrix}
$$

Next, we find the determinant of $AB$:

$$
\det(AB) = (2)(3) - (3)(0) = 6
$$

Using the $2 \times 2$ inverse formula:

$$
(AB)^{-1} = \frac{1}{6} \begin{pmatrix} 3 & -3 \\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\ 0 & \frac{1}{3} \end{pmatrix}
$$

---

### 2. Compute $B^{-1}A^{-1}$

First, we find the individual inverses $A^{-1}$ and $B^{-1}$:

* For $A$: $\det(A) = (1)(1) - (1)(0) = 1$, so

$$
A^{-1} = \frac{1}{1} \begin{pmatrix} 1 & -1 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -1 \\\ 0 & 1 \end{pmatrix}
$$

* For $B$: $\det(B) = (2)(3) - (0)(0) = 6$, so

$$
B^{-1} = \frac{1}{6} \begin{pmatrix} 3 & 0 \\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\\ 0 & \frac{1}{3} \end{pmatrix}
$$

Now, we multiply $B^{-1}$ by $A^{-1}$:

$$
B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\\ 0 & \frac{1}{3} \end{pmatrix} \begin{pmatrix} 1 & -1 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \left(\frac{1}{2}\right)(1) + (0)(0) & \left(\frac{1}{2}\right)(-1) + (0)(1) \\\ (0)(1) + \left(\frac{1}{3}\right)(0) & (0)(-1) + \left(\frac{1}{3}\right)(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\ 0 & \frac{1}{3} \end{pmatrix}
$$

---

### 3. Comparison and Meaning of the Reversed Order

Comparing both results confirms that:

$$
(AB)^{-1} = B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\ 0 & \frac{1}{3} \end{pmatrix}
$$

**Meaning of the Reversed Order:**

* **Algebraic cancellation:** Matrix multiplication is not commutative, so the inner factors must cancel first when multiplying $(AB)$ by its inverse:

$$
(AB)(B^{-1}A^{-1}) = A(B B^{-1})A^{-1} = A I A^{-1} = A A^{-1} = I
$$

* **Operational interpretation ("socks and shoes" principle):** Applying the product $AB$ to a vector $x$ means first applying transformation $B$, and then applying transformation $A$ to the result $A(Bx)$. To undo this sequence and return to $x$, you must undo the last action first ($A^{-1}$) and then undo the first action ($B^{-1}$), resulting in $B^{-1}(A^{-1}y) = (B^{-1}A^{-1})y$.

---

### Conclusion

* Both $(AB)^{-1}$ and $B^{-1}A^{-1}$ evaluate to:

$$
(AB)^{-1} = B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\\ 0 & \frac{1}{3} \end{pmatrix}
$$

* Inverses reverse the order of matrix multiplication because undoing a composition of linear transformations requires reversing each step in last-in, first-out order.
