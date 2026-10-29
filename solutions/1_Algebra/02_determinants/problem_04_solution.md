# Exercise 4. Triangular Matrix

**Given Matrix:**

$$
A = \begin{pmatrix} 2 & 4 & 1 \\\ 0 & -3 & 5 \\\ 0 & 0 & 7 \end{pmatrix}
$$

Matrix $A$ is an **upper triangular matrix** because all entries strictly below the main diagonal are equal to zero ($a_{ij} = 0$ for all $i > j$).

---

### **1. General Rule for Arbitrary Triangular Matrices**

For any $n \times n$ triangular matrix $T$ (whether upper triangular, lower triangular, or diagonal), the determinant is simply the **product of its diagonal entries**:

$$
\det(T) = t_{11} \cdot t_{22} \cdots t_{nn} = \prod_{i=1}^n t_{ii}
$$

---

### **2. Computation Without Expanding**

Applying this rule directly to matrix $A$:

$$
\det(A) = a_{11} \cdot a_{22} \cdot a_{33} = (2) \cdot (-3) \cdot (7)
$$

$$
\det(A) = -42
$$

---

### **3. Explanation Using this Example**

This property can be understood by considering what happens if we were to compute the determinant via cofactor expansion:

1. **Expansion along the first column:**  
   The first column contains only one non-zero entry, which is the diagonal element $a_{11} = 2$:

$$
\det(A) = 2 \cdot \det\begin{pmatrix} -3 & 5 \\\ 0 & 7 \end{pmatrix} - 0 + 0
$$

2. **Determinant of the remaining $2 \times 2$ submatrix:**  
   The resulting $2 \times 2$ matrix is also upper triangular. Its determinant is again obtained by multiplying its diagonal elements:

$$
\det\begin{pmatrix} -3 & 5 \\\ 0 & 7 \end{pmatrix} = (-3)(7) - (5)(0) = (-3)(7)
$$

3. **Combined product:**  
   Substituting this back into the expansion yields:

$$
\det(A) = (2) \cdot (-3) \cdot (7) = -42
$$

Because all off-diagonal terms involving zeros vanish at each successive stage of expansion, only the product of the diagonal elements survives.
