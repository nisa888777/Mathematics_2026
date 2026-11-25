# Exercise 10. Columns of a Matrix Product

## Question

Given

$$
A = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 2 \\\ -1 & 0 \\\ 3 & 1 \end{pmatrix}.
$$

Denote the columns of $B$ by $b_1, b_2$.

1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

---

## Solution

The columns of the $3 \times 2$ matrix $B$ are:

$$
b_1 = \begin{pmatrix} 1 \\\ -1 \\\ 3 \end{pmatrix}, \qquad b_2 = \begin{pmatrix} 2 \\\ 0 \\\ 1 \end{pmatrix}
$$

---

### 1. Compute $Ab_1$ and $Ab_2$

* **Compute $Ab_1$:**

$$
Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\\ -1 \\\ 3 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(-1) + 0(3) \\\ 0(1) + 1(-1) + 1(3) \end{pmatrix} = \begin{pmatrix} 1 - 2 + 0 \\\ 0 - 1 + 3 \end{pmatrix} = \begin{pmatrix} -1 \\\ 2 \end{pmatrix}
$$

* **Compute $Ab_2$:**

$$
Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\\ 0 \\\ 1 \end{pmatrix} = \begin{pmatrix} 1(2) + 2(0) + 0(1) \\\ 0(2) + 1(0) + 1(1) \end{pmatrix} = \begin{pmatrix} 2 + 0 + 0 \\\ 0 + 0 + 1 \end{pmatrix} = \begin{pmatrix} 2 \\\ 1 \end{pmatrix}
$$

---

### 2. Compute the Matrix $AB$

Since $A$ is $2 \times 3$ and $B$ is $3 \times 2$, their product $AB$ is a $2 \times 2$ matrix whose $(i, j)$-entry is the dot product of Row $i$ of $A$ and Column $j$ of $B$:

$$
AB = \begin{pmatrix} 1 & 2 & 0 \\\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\\ -1 & 0 \\\ 3 & 1 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(-1) + 0(3) & 1(2) + 2(0) + 0(1) \\\ 0(1) + 1(-1) + 1(3) & 0(2) + 1(0) + 1(1) \end{pmatrix} = \begin{pmatrix} -1 & 2 \\\ 2 & 1 \end{pmatrix}
$$

---

### 3. Comparison and Explanation

* **Comparison:** Comparing the results from Parts 1 and 2 shows that the first column of $AB$ equals $Ab_1$ and the second column of $AB$ equals $Ab_2$:

$$
AB = \begin{pmatrix} -1 & 2 \\\ 2 & 1 \end{pmatrix} = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}
$$

* **Explanation:** By the definition of matrix multiplication, the $(i, j)$-th entry of $AB$ is computed using only the $i$-th row of $A$ and the $j$-th column $b_j$ of $B$. Collecting all entries in the $j$-th column of $AB$ (for $i = 1, \dots, m$) performs the exact same row-by-column dot products as multiplying the entire matrix $A$ by the single column vector $b_j$. Consequently, matrix multiplication acts column-by-column on the right factor:

$$
A \begin{pmatrix} b_1 & b_2 \end{pmatrix} = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}
$$

---

### Conclusion

* **Matrix-vector products:** $Ab_1 = (-1, 2)^T$ and $Ab_2 = (2, 1)^T$.
* **Matrix product:**

$$
AB = \begin{pmatrix} -1 & 2 \\\ 2 & 1 \end{pmatrix}
$$

* **Column property:** Because each column of $AB$ is formed by taking dot products of the rows of $A$ with the corresponding column of $B$, the $j$-th column of $AB$ is always equal to $Ab_j$.
