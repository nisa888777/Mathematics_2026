# Exercise 15. Combining Determinant Properties

## Question

Let $A$ and $B$ be invertible $2 \times 2$ matrices with

$$
\det A = -2, \qquad \det B = 3.
$$

Without finding the entries of the matrices, compute

$$
\det \left(B^{-1} A^T B\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

---

## Solution

We are given two invertible $2 \times 2$ matrices $A$ and $B$ with $\det(A) = -2$ and $\det(B) = 3$. We evaluate $\det(B^{-1} A^T B)$ step by step using fundamental properties of determinants.

---

### Step 1: Apply the Multiplicative Property of Determinants

* **Property 1 (Product Rule):**  
  For any square matrices $X, Y, Z$ of the same size, the determinant of a product equals the product of their determinants:

$$
\det(XYZ) = \det(X) \cdot \det(Y) \cdot \det(Z)
$$

Applying this property to $B^{-1} A^T B$ gives:

$$
\det\left(B^{-1} A^T B\right) = \det\left(B^{-1}\right) \cdot \det\left(A^T\right) \cdot \det(B)
$$

---

### Step 2: Apply the Inverse and Transpose Properties

* **Property 2 (Inverse Matrix Rule):**  
  For any invertible square matrix $B$, the determinant of its inverse is the reciprocal of its determinant:

$$
\det\left(B^{-1}\right) = \frac{1}{\det(B)}
$$

* **Property 3 (Transpose Rule):**  
  Transposing a square matrix does not change its determinant:

$$
\det\left(A^T\right) = \det(A)
$$

Substituting both rules into our expression:

$$
\det\left(B^{-1} A^T B\right) = \frac{1}{\det(B)} \cdot \det(A) \cdot \det(B)
$$

---

### Step 3: Why the Factors Involving $B$ Cancel and Final Calculation

* **Explanation of Cancellation:**  
  Because determinants are ordinary real numbers (scalars), multiplication is commutative. Furthermore, since $B$ is invertible, $\det(B) = 3 \neq 0$, meaning $\det(B^{-1}) = \frac{1}{\det(B)}$ is well-defined and non-zero. Therefore, the scalar factor $\frac{1}{\det(B)}$ and $\det(B)$ are multiplicative inverses in $\mathbb{R}$ and cancel out directly:

$$
\frac{1}{\det(B)} \cdot \det(B) = \frac{1}{3} \cdot 3 = 1
$$

  (Geometrically and algebraically, conjugation $B^{-1} M B$ represents the same linear transformation $M$ expressed in a different basis, which preserves the volume scaling factor $\det(M)$.)

* **Final Numerical Substitution:**  
  Substituting $\det(A) = -2$ and $\det(B) = 3$:

$$
\det\left(B^{-1} A^T B\right) = \frac{1}{3} \cdot (-2) \cdot 3 = -2
$$

---

### Conclusion

* **Order of Properties Used:**
  1. **Product rule:** $\det(B^{-1} A^T B) = \det(B^{-1})\det(A^T)\det(B)$
  2. **Inverse rule:** $\det(B^{-1}) = \frac{1}{\det(B)}$
  3. **Transpose rule:** $\det(A^T) = \det(A)$
* **Why $B$ Cancels:** Since determinants are non-zero real numbers for invertible matrices, $\det(B^{-1}) = \frac{1}{\det(B)}$ and $\det(B)$ are reciprocal scalars whose product equals $1$.
* **Final Value:**

$$
\det\left(B^{-1} A^T B\right) = -2
$$
