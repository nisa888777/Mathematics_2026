# Exercise 12. Finding Inverses Without Starting from Scratch

## Question

It is known that

$$
A^{-1} = \begin{pmatrix} 2 & -1 \\\ -3 & 2 \end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

---

## Solution

We are given the inverse matrix:

$$
A^{-1} = \begin{pmatrix} 2 & -1 \\\ -3 & 2 \end{pmatrix}
$$

Rather than computing $A$ first, we apply the fundamental algebraic properties of matrix inverses directly.

---

### 1. Compute $(3A)^{-1}$

**Property (Scalar Multiple of an Invertible Matrix):** For any non-zero scalar $c \neq 0$ and invertible matrix $A$, the inverse of $cA$ is given by:

$$
(cA)^{-1} = \frac{1}{c} A^{-1}
$$

Justification: $(cA)\left(\frac{1}{c} A^{-1}\right) = \left(c \cdot \frac{1}{c}\right)(A A^{-1}) = 1 \cdot I = I$.

Applying this property with $c = 3$:

$$
(3A)^{-1} = \frac{1}{3} A^{-1} = \frac{1}{3} \begin{pmatrix} 2 & -1 \\\ -3 & 2 \end{pmatrix} = \begin{pmatrix} \frac{2}{3} & -\frac{1}{3} \\\ -1 & \frac{2}{3} \end{pmatrix}
$$

---

### 2. Compute $(A^T)^{-1}$

**Property (Inverse of a Transpose):** For any invertible matrix $A$, its transpose $A^T$ is also invertible, and the inverse of the transpose equals the transpose of the inverse:

$$
(A^T)^{-1} = (A^{-1})^T
$$

Justification: Taking the transpose of $A A^{-1} = I$ yields $(A A^{-1})^T = I^T \implies (A^{-1})^T A^T = I$.

Taking the transpose of the given $A^{-1}$:

$$
(A^T)^{-1} = (A^{-1})^T = \begin{pmatrix} 2 & -1 \\\ -3 & 2 \end{pmatrix}^T = \begin{pmatrix} 2 & -3 \\\ -1 & 2 \end{pmatrix}
$$

---

### 3. Compute $(A^2)^{-1}$

**Property (Inverse of a Matrix Power / Product):** For any invertible matrix $A$, $(AB)^{-1} = B^{-1}A^{-1}$. Setting $B = A$ gives the inverse of a square:

$$
(A^2)^{-1} = (A \cdot A)^{-1} = A^{-1} A^{-1} = (A^{-1})^2
$$

Justification: $A^2 (A^{-1})^2 = A(A A^{-1})A^{-1} = A I A^{-1} = A A^{-1} = I$.

Multiplying $A^{-1}$ by itself:

$$
(A^2)^{-1} = (A^{-1})^2 = \begin{pmatrix} 2 & -1 \\\ -3 & 2 \end{pmatrix} \begin{pmatrix} 2 & -1 \\\ -3 & 2 \end{pmatrix} = \begin{pmatrix} (2)(2) + (-1)(-3) & (2)(-1) + (-1)(2) \\\ (-3)(2) + (2)(-3) & (-3)(-1) + (2)(2) \end{pmatrix} = \begin{pmatrix} 4 + 3 & -2 - 2 \\\ -6 - 6 & 3 + 4 \end{pmatrix} = \begin{pmatrix} 7 & -4 \\\ -12 & 7 \end{pmatrix}
$$

---

### Conclusion

Using inverse properties directly from $A^{-1}$ without computing $A$:

* Scalar multiple inverse:

$$
(3A)^{-1} = \frac{1}{3}A^{-1} = \begin{pmatrix} \frac{2}{3} & -\frac{1}{3} \\\ -1 & \frac{2}{3} \end{pmatrix}
$$

* Transpose inverse:

$$
(A^T)^{-1} = (A^{-1})^T = \begin{pmatrix} 2 & -3 \\\ -1 & 2 \end{pmatrix}
$$

* Square inverse:

$$
(A^2)^{-1} = (A^{-1})^2 = \begin{pmatrix} 7 & -4 \\\ -12 & 7 \end{pmatrix}
$$

