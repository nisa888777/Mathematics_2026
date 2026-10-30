# Exercise 7. Using Properties Instead of Recomputing

## Question

Suppose that for a $3 \times 3$ matrix, $\det(A) = -4$. Compute

$$
\det(2A), \quad \det(A^T), \quad \det(A^2), \quad \det(-A).
$$

Justify each answer using the appropriate property.

---

## Solution

We are given an $n \times n$ matrix $A$ with size $n = 3$ and determinant $\det(A) = -4$. We evaluate each expression using the fundamental properties of determinants.

---

### 1. Computation of $\det(2A)$

* **Property (Scalar Multiplication):**  
  For any $n \times n$ matrix $A$ and any scalar $c$, multiplying the entire matrix by $c$ scales each of its $n$ rows by $c$. Therefore, the factor $c$ is factored out $n$ times:

$$
\det(cA) = c^n \det(A)
$$

* **Calculation:**  
  Here, $c = 2$ and $n = 3$:

$$
\det(2A) = 2^3 \cdot \det(A) = 8 \cdot (-4) = -32
$$

---

### 2. Computation of $\det(A^T)$

* **Property (Transpose):**  
  The determinant of a matrix is equal to the determinant of its transpose, because taking the transpose interchanges rows and columns without changing the values of the terms in the determinant expansion:

$$
\det(A^T) = \det(A)
$$

* **Calculation:**  

$$
\det(A^T) = -4
$$

---

### 3. Computation of $\det(A^2)$

* **Property (Multiplicative Property):**  
  The determinant of the product of two square matrices is the product of their determinants ($\det(AB) = \det(A)\det(B)$). Consequently, for any positive integer power:

$$
\det(A^k) = (\det(A))^k
$$

* **Calculation:**  
  For $k = 2$:

$$
\det(A^2) = (\det(A))^2 = (-4)^2 = 16
$$

---

### 4. Computation of $\det(-A)$

* **Property (Negation of an Odd-Dimensional Matrix):**  
  Negating a matrix corresponds to multiplying it by the scalar $c = -1$. Applying the scalar multiplication rule $\det(cA) = c^n \det(A)$ with $n = 3$:

$$
\det(-A) = (-1)^n \det(A) = (-1)^3 \det(A) = -\det(A)
$$

* **Calculation:**  

$$
\det(-A) = -(-4) = 4
$$

---

### Conclusion

* $\det(2A) = -32$ (using $\det(cA) = c^n \det(A)$ with $n = 3$)
* $\det(A^T) = -4$ (using $\det(A^T) = \det(A)$)
* $\det(A^2) = 16$ (using $\det(A^2) = (\det(A))^2$)
* $\det(-A) = 4$ (using $\det(-A) = (-1)^3 \det(A)$)
