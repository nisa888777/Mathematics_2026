# Exercise 5. Matrix Times Vector

**Given:**

$$
A = \begin{pmatrix} 2 & -1 \\\ 1 & 3 \end{pmatrix}, \quad \mathbf{x} = \begin{pmatrix} 4 \\\ 2 \end{pmatrix}
$$

Matrix $A$ has dimension $2 \times 2$ and vector $\mathbf{x}$ has dimension $2 \times 1$. The product $A\mathbf{x}$ results in a $2 \times 1$ vector.

---

### **1. Compute $A\mathbf{x}$**

Evaluating using the standard row-by-column rule:

$$
A\mathbf{x} = \begin{pmatrix} 2 & -1 \\\ 1 & 3 \end{pmatrix} \begin{pmatrix} 4 \\\ 2 \end{pmatrix} = \begin{pmatrix} (2)(4) + (-1)(2) \\\ (1)(4) + (3)(2) \end{pmatrix} = \begin{pmatrix} 8 - 2 \\\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\\ 10 \end{pmatrix}
$$

---

### **2. Linear Combination of the Columns of $A$**

The product $A\mathbf{x}$ can be written as a linear combination of the columns of matrix $A$, weighted by the corresponding components of vector $\mathbf{x}$:

$$
\mathbf{a}_1 = \begin{pmatrix} 2 \\\ 1 \end{pmatrix}, \quad \mathbf{a}_2 = \begin{pmatrix} -1 \\\ 3 \end{pmatrix}, \quad x_1 = 4, \quad x_2 = 2
$$

Expressing $A\mathbf{x}$ as a linear combination:

$$
A\mathbf{x} = x_1 \mathbf{a}_1 + x_2 \mathbf{a}_2 = 4 \begin{pmatrix} 2 \\\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\\ 3 \end{pmatrix}
$$

Verifying the result:

$$
4 \begin{pmatrix} 2 \\\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\\ 3 \end{pmatrix} = \begin{pmatrix} 8 \\\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\\ 6 \end{pmatrix} = \begin{pmatrix} 8 - 2 \\\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\\ 10 \end{pmatrix}
$$
