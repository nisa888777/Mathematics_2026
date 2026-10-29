# Exercise 12. Formula for a Matrix Power

**Given Matrix:**

$$
A = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix}
$$

---

### **1. Compute Successive Powers: $A^2, A^3,$ and $A^4$**

* **Compute $A^2 = A \cdot A$:**

$$
A^2 = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1)(1) + (1)(0) & (1)(1) + (1)(1) \\\ (0)(1) + (1)(0) & (0)(1) + (1)(1) \end{pmatrix} = \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix}
$$

* **Compute $A^3 = A^2 \cdot A$:**

$$
A^3 = \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1)(1) + (2)(0) & (1)(1) + (2)(1) \\\ (0)(1) + (1)(0) & (0)(1) + (1)(1) \end{pmatrix} = \begin{pmatrix} 1 & 3 \\\ 0 & 1 \end{pmatrix}
$$

* **Compute $A^4 = A^3 \cdot A$:**

$$
A^4 = \begin{pmatrix} 1 & 3 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (1)(1) + (3)(0) & (1)(1) + (3)(1) \\\ (0)(1) + (1)(0) & (0)(1) + (1)(1) \end{pmatrix} = \begin{pmatrix} 1 & 4 \\\ 0 & 1 \end{pmatrix}
$$

---

### **2. Conjecture for $A^n$**

Observing the computed powers:

$$
A^1 = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix}, \quad A^2 = \begin{pmatrix} 1 & 2 \\\ 0 & 1 \end{pmatrix}, \quad A^3 = \begin{pmatrix} 1 & 3 \\\ 0 & 1 \end{pmatrix}, \quad A^4 = \begin{pmatrix} 1 & 4 \\\ 0 & 1 \end{pmatrix}
$$

We conjecture that for any positive integer $n \ge 1$:

$$
A^n = \begin{pmatrix} 1 & n \\\ 0 & 1 \end{pmatrix}
$$

---

### **3. Proof / Induction Step ($n \to n + 1$)**

* **Induction Hypothesis:**  
  Assume the formula holds for an arbitrary positive integer $n$:

$$
A^n = \begin{pmatrix} 1 & n \\\ 0 & 1 \end{pmatrix}
$$

* **Inductive Step:**  
  Multiply $A^n$ by $A$ to compute $A^{n+1}$:

$$
A^{n+1} = A^n \cdot A = \begin{pmatrix} 1 & n \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix}
$$

Evaluating each entry by standard matrix multiplication:
* Row 1, Column 1: $(1)(1) + (n)(0) = 1 + 0 = 1$
* Row 1, Column 2: $(1)(1) + (n)(1) = 1 + n = n + 1$
* Row 2, Column 1: $(0)(1) + (1)(0) = 0 + 0 = 0$
* Row 2, Column 2: $(0)(1) + (1)(1) = 0 + 1 = 1$

$$
A^{n+1} = \begin{pmatrix} 1 & n+1 \\\ 0 & 1 \end{pmatrix}
$$

**Conclusion:**  
Multiplying by $A$ preserves the main diagonal entries as $1$ and the lower-left entry as $0$, while adding $1$ to the upper-right entry ($n \to n+1$). Thus, by mathematical induction, the formula holds for all integers $n \ge 1$:

$$
A^n = \begin{pmatrix} 1 & n \\\ 0 & 1 \end{pmatrix}
$$
