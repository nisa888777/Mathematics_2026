# Exercise 15. Associativity of Multiplication and Different Calculation Paths

**Given Matrices:**

$$
A = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 0 \\\ 2 & 1 \\\ -1 & 3 \end{pmatrix}, \quad C = \begin{pmatrix} 2 & 1 \\\ 0 & -1 \end{pmatrix}
$$

* Matrix $A$ has dimension $2 \times 3$.
* Matrix $B$ has dimension $3 \times 2$.
* Matrix $C$ has dimension $2 \times 2$.

---

### **1. Compute $(AB)C$**

* **Step 1: Compute the product $AB$ ($2 \times 3$ by $3 \times 2 \to 2 \times 2$):**

$$
AB = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\\ 2 & 1 \\\ -1 & 3 \end{pmatrix}
$$

Evaluating each entry:
* Row 1, Column 1: $(1)(1) + (2)(2) + (0)(-1) = 1 + 4 + 0 = 5$
* Row 1, Column 2: $(1)(0) + (2)(1) + (0)(3) = 0 + 2 + 0 = 2$
* Row 2, Column 1: $(0)(1) + (1)(2) + (1)(-1) = 0 + 2 - 1 = 1$
* Row 2, Column 2: $(0)(0) + (1)(1) + (1)(3) = 0 + 1 + 3 = 4$

$$
AB = \begin{pmatrix} 5 & 2 \\\ 1 & 4 \end{pmatrix}
$$

* **Step 2: Multiply $(AB)$ by $C$ ($2 \times 2$ by $2 \times 2 \to 2 \times 2$):**

$$
(AB)C = \begin{pmatrix} 5 & 2 \\\ 1 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\\ 0 & -1 \end{pmatrix}
$$

Evaluating each entry:
* Row 1, Column 1: $(5)(2) + (2)(0) = 10 + 0 = 10$
* Row 1, Column 2: $(5)(1) + (2)(-1) = 5 - 2 = 3$
* Row 2, Column 1: $(1)(2) + (4)(0) = 2 + 0 = 2$
* Row 2, Column 2: $(1)(1) + (4)(-1) = 1 - 4 = -3$

$$
(AB)C = \begin{pmatrix} 10 & 3 \\\ 2 & -3 \end{pmatrix}
$$

---

### **2. Compute $A(BC)$**

* **Step 1: Compute the product $BC$ ($3 \times 2$ by $2 \times 2 \to 3 \times 2$):**

$$
BC = \begin{pmatrix} 1 & 0 \\\ 2 & 1 \\\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & 1 \\\ 0 & -1 \end{pmatrix}
$$

Evaluating each entry:
* Row 1, Column 1: $(1)(2) + (0)(0) = 2 + 0 = 2$
* Row 1, Column 2: $(1)(1) + (0)(-1) = 1 + 0 = 1$
* Row 2, Column 1: $(2)(2) + (1)(0) = 4 + 0 = 4$
* Row 2, Column 2: $(2)(1) + (1)(-1) = 2 - 1 = 1$
* Row 3, Column 1: $(-1)(2) + (3)(0) = -2 + 0 = -2$
* Row 3, Column 2: $(-1)(1) + (3)(-1) = -1 - 3 = -4$

$$
BC = \begin{pmatrix} 2 & 1 \\\ 4 & 1 \\\ -2 & -4 \end{pmatrix}
$$

* **Step 2: Multiply $A$ by $(BC)$ ($2 \times 3$ by $3 \times 2 \to 2 \times 2$):**

$$
A(BC) = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\\ 4 & 1 \\\ -2 & -4 \end{pmatrix}
$$

Evaluating each entry:
* Row 1, Column 1: $(1)(2) + (2)(4) + (0)(-2) = 2 + 8 + 0 = 10$
* Row 1, Column 2: $(1)(1) + (2)(1) + (0)(-4) = 1 + 2 + 0 = 3$
* Row 2, Column 1: $(0)(2) + (1)(4) + (1)(-2) = 0 + 4 - 2 = 2$
* Row 2, Column 2: $(0)(1) + (1)(1) + (1)(-4) = 0 + 1 - 4 = -3$

$$
A(BC) = \begin{pmatrix} 10 & 3 \\\ 2 & -3 \end{pmatrix}
$$

---

### **3. Comparison of Results and Operation Count**

* **Result Comparison:**

$$
(AB)C = A(BC) = \begin{pmatrix} 10 & 3 \\\ 2 & -3 \end{pmatrix}
$$

Both calculation paths yield the exact same resulting matrix.

* **Count of Intermediate Operations:**  
  Multiplying a matrix of size $m \times k$ by a matrix of size $k \times p$ requires $m \times k \times p$ scalar multiplications:

  1. **Path 1: $(AB)C$**
     * $AB$ requires $2 \times 3 \times 2 = 12$ multiplications.
     * $(AB)C$ requires $2 \times 2 \times 2 = 8$ multiplications.
     * **Total:** $12 + 8 = 20$ scalar multiplications.

  2. **Path 2: $A(BC)$**
     * $BC$ requires $3 \times 2 \times 2 = 12$ multiplications.
     * $A(BC)$ requires $2 \times 3 \times 2 = 12$ multiplications.
     * **Total:** $12 + 12 = 24$ scalar multiplications.

Computing $(AB)C$ is computationally more efficient than $A(BC)$ because it involves fewer total arithmetic operations ($20$ vs $24$ multiplications).

---

### **4. Meaning of Associativity in this Example**

* **Algebraic Meaning:**  
  Associativity states that for any matrices where products are defined, $(AB)C = A(BC)$. The placement of parentheses does not alter the final linear transformation or the resulting matrix values.
* **Computational Implication:**  
  While the mathematical result is identical, the intermediate matrices and total computational work depend heavily on the evaluation order (a core concept behind optimal matrix chain multiplication algorithms).
