# Exercise 9. Area and the Determinant

## Question

The vectors

$$
u = \begin{pmatrix} 3 \\\ 1 \end{pmatrix}, \quad v = \begin{pmatrix} 1 \\\ 4 \end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

---

## Solution

The geometric area of a parallelogram spanned by two vectors in $\mathbb{R}^2$ is given by the absolute value of the determinant of the matrix formed by placing the vectors as columns (or rows).

---

### 1. Parallelogram Area with Vectors in Order $(u, v)$

Construct matrix $M_1$ with vectors $u$ and $v$ as columns:

$$
M_1 = \begin{pmatrix} 3 & 1 \\\ 1 & 4 \end{pmatrix}
$$

Compute the determinant:

$$
\det(M_1) = (3)(4) - (1)(1) = 12 - 1 = 11
$$

Since area is a non-negative geometric quantity:

$$
\text{Area} = |\det(M_1)| = |11| = 11
$$

---

### 2. Parallelogram Area with Reversed Order $(v, u)$

Construct matrix $M_2$ with the reversed order of vectors as columns:

$$
M_2 = \begin{pmatrix} 1 & 3 \\\ 4 & 1 \end{pmatrix}
$$

Compute the determinant:

$$
\det(M_2) = (1)(1) - (3)(4) = 1 - 12 = -11
$$

Compute the area:

$$
\text{Area} = |\det(M_2)| = |-11| = 11
$$

---

### 3. Explanation of Changes and Invariants

* **What changes in the determinant:**  
  Reversing the order of the vectors corresponds to swapping two columns of the matrix. A fundamental property of determinants states that interchanging any two columns (or rows) multiplies the determinant by $-1$:

$$
\det(M_2) = -\det(M_1) = -11
$$

  The sign of the determinant indicates the **orientation** of the vector pair (an ordered basis):
  * $(u, v)$ has a positive, counterclockwise orientation ($\det > 0$).
  * $(v, u)$ has a negative, clockwise orientation ($\det < 0$).

* **What does not change in the area:**  
  The geometric parallelogram itself in the plane remains identical regardless of the order in which its spanning vectors are listed. Since geometric area is defined as the absolute magnitude of the signed determinant ($|\det|$), the area remains invariant:

$$
\text{Area} = |\det(M_1)| = |\det(M_2)| = 11
$$

---

### Conclusion

* **Area of the parallelogram:**

$$
\text{Area} = 11
$$

* **Determinant with order $(u, v)$:** $\det(M_1) = 11$
* **Determinant with order $(v, u)$:** $\det(M_2) = -11$
* **Summary:** The determinant changes sign due to column exchange (reflecting reversed orientation), while the area remains unchanged because area depends strictly on the absolute value.
