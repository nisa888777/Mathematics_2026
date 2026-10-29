# Exercise 7. Identity Matrix, Zero Matrix, and Powers

**Given Matrix:**

$$
A = \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix}
$$

The corresponding $2 \times 2$ identity matrix $I$ and zero matrix $0$ are:

$$
I = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix}, \quad 0 = \begin{pmatrix} 0 & 0 \\\ 0 & 0 \end{pmatrix}
$$

---

### **1. Compute $AI$, $IA$, and $A + 0$**

* **Product $AI$:**

$$
AI = \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (2)(1) + (1)(0) & (2)(0) + (1)(1) \\\ (0)(1) + (2)(0) & (0)(0) + (2)(1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} = A
$$

* **Product $IA$:**

$$
IA = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (1)(2) + (0)(0) & (1)(1) + (0)(2) \\\ (0)(2) + (1)(0) & (0)(1) + (1)(2) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} = A
$$

* **Sum $A + 0$:**

$$
A + 0 = \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 2 + 0 & 1 + 0 \\\ 0 + 0 & 2 + 0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} = A
$$

---

### **2. Compute $A^2$ and $A^3$**

* **$A^2 = A \cdot A$:**

$$
A^2 = \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (2)(2) + (1)(0) & (2)(1) + (1)(2) \\\ (0)(2) + (2)(0) & (0)(1) + (2)(2) \end{pmatrix} = \begin{pmatrix} 4 & 4 \\\ 0 & 4 \end{pmatrix}
$$

* **$A^3 = A^2 \cdot A$:**

$$
A^3 = \begin{pmatrix} 4 & 4 \\\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} (4)(2) + (4)(0) & (4)(1) + (4)(2) \\\ (0)(2) + (4)(0) & (0)(1) + (4)(2) \end{pmatrix} = \begin{pmatrix} 8 & 12 \\\ 0 & 8 \end{pmatrix}
$$

---

### **3. Roles of $I$ and $0$**

* **Identity Matrix ($I$):** Acts as the **multiplicative neutral element** (identity element) in matrix algebra. Multiplying any compatible matrix by $I$ on either side leaves the matrix unchanged ($AI = IA = A$).
* **Zero Matrix ($0$):** Acts as the **additive neutral element** (additive identity). Adding the zero matrix to any matrix of the same dimension leaves the matrix unchanged ($A + 0 = A$).

---

### **4. Pattern in Successive Powers of $A$**

Observing the computed powers:

$$
A^1 = \begin{pmatrix} 2 & 1 \\\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 2^1 & 1 \cdot 2^0 \\\ 0 & 2^1 \end{pmatrix}
$$

$$
A^2 = \begin{pmatrix} 4 & 4 \\\ 0 & 4 \end{pmatrix} = \begin{pmatrix} 2^2 & 2 \cdot 2^1 \\\ 0 & 2^2 \end{pmatrix}
$$

$$
A^3 = \begin{pmatrix} 8 & 12 \\\ 0 & 8 \end{pmatrix} = \begin{pmatrix} 2^3 & 3 \cdot 2^2 \\\ 0 & 2^3 \end{pmatrix}
$$

In general, for any positive integer $n \ge 1$:

$$
A^n = \begin{pmatrix} 2^n & n \cdot 2^{n-1} \\\ 0 & 2^n \end{pmatrix}
$$

* The main diagonal entries are powers of $2$ ($2^n$).
* The lower-left entry remains $0$.
* The upper-right entry follows the pattern $n \cdot 2^{n-1}$.
