# Exercise 4. Matrix Multiplication and Noncommutativity

**Given Matrices:**

$$
A = \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 2 & 0 \\\ 3 & 1 \end{pmatrix}
$$

Both matrices have size $2 \times 2$.

---

### **1. Compute $AB$**

$$
AB = \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\\ 3 & 1 \end{pmatrix}
$$

Evaluating each entry by multiplying rows by columns:
- Row 1, Column 1: $(1)(2) + (2)(3) = 2 + 6 = 8$
- Row 1, Column 2: $(1)(0) + (2)(1) = 0 + 2 = 2$
- Row 2, Column 1: $(0)(2) + (1)(3) = 0 + 3 = 3$
- Row 2, Column 2: $(0)(0) + (1)(1) = 0 + 1 = 1$

$$
AB = \begin{pmatrix} 8 & 2 \\\ 3 & 1 \end{pmatrix}
$$

---

### **2. Compute $BA$**

$$
BA = \begin{pmatrix} 2 & 0 \\\ 3 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix}
$$

Evaluating each entry by multiplying rows by columns:
- Row 1, Column 1: $(2)(1) + (0)(0) = 2 + 0 = 2$
- Row 1, Column 2: $(2)(2) + (0)(1) = 4 + 0 = 4$
- Row 2, Column 1: $(3)(1) + (1)(0) = 3 + 0 = 3$
- Row 2, Column 2: $(3)(2) + (1)(1) = 6 + 1 = 7$

$$
BA = \begin{pmatrix} 2 & 4 \\\ 3 & 7 \end{pmatrix}
$$

---

### **3. Is $AB = BA$?**

Comparing the results:

$$
\begin{pmatrix} 8 & 2 \\\ 3 & 1 \end{pmatrix} \neq \begin{pmatrix} 2 & 4 \\\ 3 & 7 \end{pmatrix}
$$

Therefore, **$AB \neq BA$**.

---

### **4. Meaning of Noncommutativity**

In ordinary scalar arithmetic, multiplication is commutative ($a \cdot b = b \cdot a$). However, matrix multiplication is generally **noncommutative**. This means that changing the order of multiplication yields completely different results ($AB \neq BA$), even when both matrices are square and the products in both orders are well-defined.
