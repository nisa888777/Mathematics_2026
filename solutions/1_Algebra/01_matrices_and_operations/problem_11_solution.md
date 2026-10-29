# Exercise 11. When Do Matrices Commute?

**Given Matrices:**

$$
A = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} a & b \\\ c & d \end{pmatrix}
$$

We want to find the conditions on the entries $a, b, c, d$ such that:

$$
AB = BA
$$

---

### **1. Compute the Products $AB$ and $BA$**

* **Product $AB$:**

$$
AB = \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\\ c & d \end{pmatrix} = \begin{pmatrix} (1)(a) + (1)(c) & (1)(b) + (1)(d) \\\ (0)(a) + (1)(c) & (0)(b) + (1)(d) \end{pmatrix} = \begin{pmatrix} a + c & b + d \\\ c & d \end{pmatrix}
$$

* **Product $BA$:**

$$
BA = \begin{pmatrix} a & b \\\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\\ 0 & 1 \end{pmatrix} = \begin{pmatrix} (a)(1) + (b)(0) & (a)(1) + (b)(1) \\\ (c)(1) + (d)(0) & (c)(1) + (d)(1) \end{pmatrix} = \begin{pmatrix} a & a + b \\\ c & c + d \end{pmatrix}
$$

---

### **2. Set $AB = BA$ and Determine the Conditions**

Equating the entries of $AB$ and $BA$:

$$
\begin{pmatrix} a + c & b + d \\\ c & d \end{pmatrix} = \begin{pmatrix} a & a + b \\\ c & c + d \end{pmatrix}
$$

This yields the following system of four equations:

1. **Row 1, Column 1:**  
   $$a + c = a \implies c = 0$$

2. **Row 1, Column 2:**  
   $$b + d = a + b \implies d = a$$

3. **Row 2, Column 1:**  
   $$c = c \implies \text{satisfied for any } c$$

4. **Row 2, Column 2:**  
   $$d = c + d \implies c = 0$$

Combining these equations, we obtain two necessary and sufficient conditions:
* $c = 0$
* $d = a$
* $b$ can be any real number ($b \in \mathbb{R}$)

---

### **3. General Form of Matrix $B$**

Substituting the conditions $c = 0$ and $d = a$ into matrix $B$:

$$
B = \begin{pmatrix} a & b \\\ 0 & a \end{pmatrix}
$$

where $a, b \in \mathbb{R}$ are arbitrary real scalars.

Alternatively, $B$ can be written as:

$$
B = a \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix} + b \begin{pmatrix} 0 & 1 \\\ 0 & 0 \end{pmatrix} = a I + b N
$$

where $I$ is the identity matrix and:

$$
N = \begin{pmatrix} 0 & 1 \\\ 0 & 0 \end{pmatrix} = A - I
$$

is a strictly upper triangular nilpotent matrix.
