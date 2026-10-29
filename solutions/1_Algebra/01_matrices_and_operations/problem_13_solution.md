# Exercise 13. A Recurrence Written in Matrix Form

**Given Matrix:**

$$
F = \begin{pmatrix} 1 & 1 \\\ 1 & 0 \end{pmatrix}
$$

The given sequence is the **Fibonacci sequence**:

$$
F_0 = 0, \quad F_1 = 1, \quad F_2 = 1, \quad F_3 = 2, \quad F_4 = 3, \quad F_5 = 5, \quad F_6 = 8, \dots
$$

defined by the recurrence relation $F_{k+1} = F_k + F_{k-1}$ for $k \ge 1$.

---

### **1. Compute Successive Powers: $F^2, F^3, F^4,$ and $F^5$**

* **Compute $F^2 = F \cdot F$:**

$$
F^2 = \begin{pmatrix} 1 & 1 \\\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (1)(1) + (1)(1) & (1)(1) + (1)(0) \\\ (1)(1) + (0)(1) & (1)(1) + (0)(0) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix}
$$

* **Compute $F^3 = F^2 \cdot F$:**

$$
F^3 = \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (2)(1) + (1)(1) & (2)(1) + (1)(0) \\\ (1)(1) + (1)(1) & (1)(1) + (1)(0) \end{pmatrix} = \begin{pmatrix} 3 & 2 \\\ 2 & 1 \end{pmatrix}
$$

* **Compute $F^4 = F^3 \cdot F$:**

$$
F^4 = \begin{pmatrix} 3 & 2 \\\ 2 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (3)(1) + (2)(1) & (3)(1) + (2)(0) \\\ (2)(1) + (1)(1) & (2)(1) + (1)(0) \end{pmatrix} = \begin{pmatrix} 5 & 3 \\\ 3 & 2 \end{pmatrix}
$$

* **Compute $F^5 = F^4 \cdot F$:**

$$
F^5 = \begin{pmatrix} 5 & 3 \\\ 3 & 2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} (5)(1) + (3)(1) & (5)(1) + (3)(0) \\\ (3)(1) + (2)(1) & (3)(1) + (2)(0) \end{pmatrix} = \begin{pmatrix} 8 & 5 \\\ 5 & 3 \end{pmatrix}
$$

---

### **2. Relationship with the Fibonacci Sequence**

Comparing the computed powers with the Fibonacci numbers:

* $F^1 = \begin{pmatrix} 1 & 1 \\\ 1 & 0 \end{pmatrix} = \begin{pmatrix} F_2 & F_1 \\\ F_1 & F_0 \end{pmatrix}$
* $F^2 = \begin{pmatrix} 2 & 1 \\\ 1 & 1 \end{pmatrix} = \begin{pmatrix} F_3 & F_2 \\\ F_2 & F_1 \end{pmatrix}$
* $F^3 = \begin{pmatrix} 3 & 2 \\\ 2 & 1 \end{pmatrix} = \begin{pmatrix} F_4 & F_3 \\\ F_3 & F_2 \end{pmatrix}$
* $F^4 = \begin{pmatrix} 5 & 3 \\\ 3 & 2 \end{pmatrix} = \begin{pmatrix} F_5 & F_4 \\\ F_4 & F_3 \end{pmatrix}$
* $F^5 = \begin{pmatrix} 8 & 5 \\\ 5 & 3 \end{pmatrix} = \begin{pmatrix} F_6 & F_5 \\\ F_5 & F_4 \end{pmatrix}$

In general, for any positive integer $n \ge 1$:

$$
F^n = \begin{pmatrix} F_{n+1} & F_n \\\ F_n & F_{n-1} \end{pmatrix}
$$

---

### **3. Compute $F \begin{pmatrix} a \\\ b \end{pmatrix}$ and Explanation**

* **Matrix-Vector Multiplication:**

$$
F \begin{pmatrix} a \\\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\\ 1 & 0 \end{pmatrix} \begin{pmatrix} a \\\ b \end{pmatrix} = \begin{pmatrix} (1)(a) + (1)(b) \\\ (1)(a) + (0)(b) \end{pmatrix} = \begin{pmatrix} a + b \\\ a \end{pmatrix}
$$

**Explanation:**  
If we represent two consecutive Fibonacci numbers as the vector:

$$
\begin{pmatrix} F_k \\\ F_{k-1} \end{pmatrix}
$$

multiplying by $F$ updates the state:

$$
F \begin{pmatrix} F_k \\\ F_{k-1} \end{pmatrix} = \begin{pmatrix} F_k + F_{k-1} \\\ F_k \end{pmatrix} = \begin{pmatrix} F_{k+1} \\\ F_k \end{pmatrix}
$$

* The top entry computes $a + b$, which generates the next term by summing the two previous consecutive terms.
* The bottom entry retains $a$, shifting the previous leading term down to become the secondary term for the next recurrence step.
