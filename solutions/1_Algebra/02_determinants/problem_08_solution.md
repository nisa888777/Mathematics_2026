# Exercise 8. Determinant of a Product

## Question

Let $A, B$ be square matrices such that $\det(A) = 3$ and $\det(B) = -5$. Compute

$$
\det(AB), \quad \det(BA) \quad \text{and, if it exists,} \quad \det(A^{-1}B).
$$

Explain why the first two results are equal even though usually $AB \neq BA$.

---

## Solution

We are given two square matrices $A$ and $B$ of the same order with determinants $\det(A) = 3$ and $\det(B) = -5$. We compute the requested determinants using the multiplicative property and the inverse property of determinants.

---

### 1. Computation of $\det(AB)$ and $\det(BA)$

* **Multiplicative Property:**  
  For any two $n \times n$ matrices $A$ and $B$, the determinant of their product equals the product of their individual determinants:

$$
\det(AB) = \det(A) \cdot \det(B)
$$

* **Calculation for $\det(AB)$:**  

$$
\det(AB) = (3) \cdot (-5) = -15
$$

* **Calculation for $\det(BA)$:**  

$$
\det(BA) = \det(B) \cdot \det(A) = (-5) \cdot (3) = -15
$$

---

### 2. Explanation of Why $\det(AB) = \det(BA)$ When $AB \neq BA$

* Matrix multiplication is generally **non-commutative** ($AB \neq BA$), meaning the product matrices $AB$ and $BA$ are usually distinct matrices with different entries.
* However, the determinant function assigns a single **scalar** (a real number) to each matrix.
* Because scalar multiplication is commutative in $\mathbb{R}$:

$$
\det(A) \cdot \det(B) = \det(B) \cdot \det(A)
$$

* Therefore:

$$
\det(AB) = \det(A) \cdot \det(B) = \det(B) \cdot \det(A) = \det(BA)
$$

Even though the resulting matrices $AB$ and $BA$ are different, they represent linear transformations that scale volume by the exact same scalar factor and reverse orientation in the same way.

---

### 3. Computation of $\det(A^{-1}B)$

* **Existence:**  
  A matrix has an inverse if and only if its determinant is non-zero. Since $\det(A) = 3 \neq 0$, the inverse matrix $A^{-1}$ exists.

* **Determinant of the Inverse:**  
  Because $A A^{-1} = I$ and $\det(I) = 1$:

$$
\det(A^{-1}) = \frac{1}{\det(A)} = \frac{1}{3}
$$

* **Calculation:**  
  Applying the multiplicative property:

$$
\det(A^{-1}B) = \det(A^{-1}) \cdot \det(B) = \left(\frac{1}{3}\right) \cdot (-5) = -\frac{5}{3}
$$

---

### Conclusion

* $\det(AB) = -15$
* $\det(BA) = -15$
* $\det(AB) = \det(BA)$ holds because the determinant maps matrices to scalars, where multiplication is commutative.
* $\det(A^{-1}B) = -\frac{5}{3}$ (exists since $\det(A) \neq 0$).
