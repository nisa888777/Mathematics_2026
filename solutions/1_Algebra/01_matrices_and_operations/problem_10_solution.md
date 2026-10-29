# Exercise 10. Columns of a Matrix Product

**Given Matrices:**

$$
A = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix}, \quad B = \begin{pmatrix} 1 & 2 \\\ -1 & 0 \\\ 3 & 1 \end{pmatrix}
$$

Matrix $A$ has dimension $2 \times 3$ and matrix $B$ has dimension $3 \times 2$.

The columns of $B$ are:

$$
\mathbf{b}_1 = \begin{pmatrix} 1 \\\ -1 \\\ 3 \end{pmatrix}, \quad \mathbf{b}_2 = \begin{pmatrix} 2 \\\ 0 \\\ 1 \end{pmatrix}
$$

---

### **1. Compute $A\mathbf{b}_1$ and $A\mathbf{b}_2$**

* **Compute $A\mathbf{b}_1$:**

$$
A\mathbf{b}_1 = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\\ -1 \\\ 3 \end{pmatrix} = \begin{pmatrix} (1)(1) + (2)(-1) + (0)(3) \\\ (0)(1) + (1)(-1) + (1)(3) \end{pmatrix} = \begin{pmatrix} 1 - 2 + 0 \\\ 0 - 1 + 3 \end{pmatrix} = \begin{pmatrix} -1 \\\ 2 \end{pmatrix}
$$

* **Compute $A\mathbf{b}_2$:**

$$
A\mathbf{b}_2 = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\\ 0 \\\ 1 \end{pmatrix} = \begin{pmatrix} (1)(2) + (2)(0) + (0)(1) \\\ (0)(2) + (1)(0) + (1)(1) \end{pmatrix} = \begin{pmatrix} 2 + 0 + 0 \\\ 0 + 0 + 1 \end{pmatrix} = \begin{pmatrix} 2 \\\ 1 \end{pmatrix}
$$

---

### **2. Compute the Matrix $AB$**

Multiplying $A$ ($2 \times 3$) and $B$ ($3 \times 2$) using the standard entry-by-entry formula:

$$
AB = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\\ -1 & 0 \\\ 3 & 1 \end{pmatrix}
$$

* Row 1, Column 1: $(1)(1) + (2)(-1) + (0)(3) = 1 - 2 + 0 = -1$
* Row 1, Column 2: $(1)(2) + (2)(0) + (0)(1) = 2 + 0 + 0 = 2$
* Row 2, Column 1: $(0)(1) + (1)(-1) + (1)(3) = 0 - 1 + 3 = 2$
* Row 2, Column 2: $(0)(2) + (1)(0) + (1)(1) = 0 + 0 + 1 = 1$

$$
AB = \begin{pmatrix} -1 & 2 \\\ 2 & 1 \end{pmatrix}
$$

---

### **3. Comparison and Explanation**

Comparing the results:

$$
AB = \begin{pmatrix} -1 & 2 \\\ 2 & 1 \end{pmatrix} = \begin{pmatrix} A\mathbf{b}_1 & A\mathbf{b}_2 \end{pmatrix}
$$

The first column of $AB$ is:

$$
A\mathbf{b}_1 = \begin{pmatrix} -1 \\\ 2 \end{pmatrix}
$$

The second column of $AB$ is:

$$
A\mathbf{b}_2 = \begin{pmatrix} 2 \\\ 1 \end{pmatrix}
$$

**Explanation:**  
By the definition of matrix multiplication partitioned by columns, multiplying a matrix $A$ by a matrix partitioned into columns:

$$
B = \begin{pmatrix} \mathbf{b}_1 & \mathbf{b}_2 \end{pmatrix}
$$

applies $A$ independently to each column:

$$
AB = A \begin{pmatrix} \mathbf{b}_1 & \mathbf{b}_2 \end{pmatrix} = \begin{pmatrix} A\mathbf{b}_1 & A\mathbf{b}_2 \end{pmatrix}
$$

Each column of the product $AB$ is formed by taking linear combinations of the columns of $A$ using the scalar weights from the corresponding column of $B$.
