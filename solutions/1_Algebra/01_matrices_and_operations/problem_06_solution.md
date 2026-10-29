# Exercise 6. Transpose

**Given Matrices:**

$$
A = \begin{pmatrix} 1 & 2 & 3 \\\ 4 & 5 & 6 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 0 \\\ 2 & 1 \\\ -1 & 3 \end{pmatrix}
$$

The dimensions are $2 \times 3$ for $A$ and $3 \times 2$ for $B$.

---

### **1. Compute the Transposes $A^T$ and $B^T$**

The transpose of a matrix interchanges its rows and columns:

* Transpose of $A$ (size $3 \times 2$):

$$
A^T = \begin{pmatrix} 1 & 4 \\\ 2 & 5 \\\ 3 & 6 \end{pmatrix}
$$

* Transpose of $B$ (size $2 \times 3$):

$$
B^T = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & 1 & 3 \end{pmatrix}
$$

---

### **2. Compute the Product $AB$**

Evaluating $AB$ (size $2 \times 2$) using standard row-by-column multiplication:

- Row 1, Column 1: $(1)(1) + (2)(2) + (3)(-1) = 1 + 4 - 3 = 2$
- Row 1, Column 2: $(1)(0) + (2)(1) + (3)(3) = 0 + 2 + 9 = 11$
- Row 2, Column 1: $(4)(1) + (5)(2) + (6)(-1) = 4 + 10 - 6 = 8$
- Row 2, Column 2: $(4)(0) + (5)(1) + (6)(3) = 0 + 5 + 18 = 23$

$$
AB = \begin{pmatrix} 2 & 11 \\\ 8 & 23 \end{pmatrix}
$$

---

### **3. Compute $(AB)^T$**

Transposing the resulting matrix $AB$:

$$
(AB)^T = \begin{pmatrix} 2 & 8 \\\ 11 & 23 \end{pmatrix}
$$

---

### **4. Compute $B^T A^T$ and Verify $(AB)^T = B^T A^T$**

Multiplying $B^T$ ($2 \times 3$) by $A^T$ ($3 \times 2$):

$$
B^T A^T = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 4 \\\ 2 & 5 \\\ 3 & 6 \end{pmatrix}
$$

Evaluating each entry:
- Row 1, Column 1: $(1)(1) + (2)(2) + (-1)(3) = 1 + 4 - 3 = 2$
- Row 1, Column 2: $(1)(4) + (2)(5) + (-1)(6) = 4 + 10 - 6 = 8$
- Row 2, Column 1: $(0)(1) + (1)(2) + (3)(3) = 0 + 2 + 9 = 11$
- Row 2, Column 2: $(0)(4) + (1)(5) + (3)(6) = 0 + 5 + 18 = 23$

$$
B^T A^T = \begin{pmatrix} 2 & 8 \\\ 11 & 23 \end{pmatrix}
$$

**Conclusion:**

$$
(AB)^T = B^T A^T = \begin{pmatrix} 2 & 8 \\\ 11 & 23 \end{pmatrix}
$$

The transpose of a matrix product reverses the order of factors, verifying $(AB)^T = B^T A^T$.
