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
  The determinant of a matrix is equal to the determinant of its transpose, because transposition interchanges rows and columns without changing the determinant expansion:

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
  The determinant of the product of two square matrices is the product of their individual determinants:

$$
\det(AB) = \det(A) \cdot \det(B)
$$

Consequently, for any positive integer power $k$:

$$
\det(A^k) = (\det(A))^k
$$

### Conclusion

* $\det(2A) = -32$ (using scalar scaling property where $c = 2$ and $n = 3$)
* $\det(A^T) = -4$ (using the transpose property where determinant remains unchanged)
* $\det(A^2) = 16$ (using the multiplicative power property)
* $\det(-A) = 4$ (using negation property for odd dimensions where factor is $(-1)^3$)


---

### 4. Computation of $\det(-A)$

* **Property (Negation of an Odd-Dimensional Matrix):**  
  Negating a matrix corresponds to multiplying the matrix by the scalar $c = -1$. Applying the scalar multiplication rule with $n = 3$:

$$
\det(-A) = (-1)^n \det(A) = (-1)^3 \det(A) = -\det(A)
$$

* **Calculation:**  

$$
\det(-A) = -(-4) = 4
$$

---

### Conclusion

* $\det(2A) = -32$ (using scalar scaling property where $c = 2$ and $n = 3$)
* $\det(A^T) = -4$ (using the transpose property where determinant remains unchanged)
* $\det(A^2) = 16$ (using the multiplicative power property)
* $\det(-A) = 4$ (using negation property for odd dimensions where factor is $(-1)^3$)
