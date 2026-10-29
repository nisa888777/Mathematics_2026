# Exercise 8. Row Operations and Their Reversibility

**Given Matrix:**

$$A = \begin{pmatrix} 1 & 2 & -1 \\\ 2 & 4 & 1 \\\ -1 & 1 & 3 \end{pmatrix}$$

Matrix $A$ has dimension $3 \times 3$.

---

### **1. Perform Row Operations in Order**

#### **Step 1: $R_2 \leftarrow R_2 - 2R_1$**

Subtract $2$ times Row 1 from Row 2:
- Entry 1: $2 - 2(1) = 2 - 2 = 0$
- Entry 2: $4 - 2(2) = 4 - 4 = 0$
- Entry 3: $1 - 2(-1) = 1 + 2 = 3$

$$A_1 = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & 0 & 3 \\\ -1 & 1 & 3 \end{pmatrix}$$

---

#### **Step 2: $R_3 \leftarrow R_3 + R_1$**

Add Row 1 to Row 3:
- Entry 1: $-1 + 1 = 0$
- Entry 2: $1 + 2 = 3$
- Entry 3: $3 + (-1) = 2$

$$A_2 = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & 0 & 3 \\\ 0 & 3 & 2 \end{pmatrix}$$

---

#### **Step 3: Interchange $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$)**

Swap the second and third rows:

$$A_3 = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & 3 & 2 \\\ 0 & 0 & 3 \end{pmatrix}$$

---

### **2. Reversing Operations**

Each elementary row operation can be undone by an inverse row operation:

1. **Forward Operation:** $R_2 \leftarrow R_2 - 2R_1$  
   **Reverse Operation:**  
   $$R_2 \leftarrow R_2 + 2R_1$$
   *(Adding $2$ times Row 1 back to Row 2 restores the original Row 2)*

2. **Forward Operation:** $R_3 \leftarrow R_3 + R_1$  
   **Reverse Operation:**  
   $$R_3 \leftarrow R_3 - R_1$$
   *(Subtract
