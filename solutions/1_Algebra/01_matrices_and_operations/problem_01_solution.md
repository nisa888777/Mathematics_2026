# Exercise 1. Matrix Size and Entries

## Question

Given

$$
A = \begin{pmatrix} 2 & -1 & 3 \\\ 0 & 4 & 5 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\\ -2 & 3 \\\ 4 & 1 \end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

---

## Solution

We are given the matrices:

$$
A = \begin{pmatrix} 2 & -1 & 3 \\\ 0 & 4 & 5 \end{pmatrix}, \qquad B = \begin{pmatrix} 1 & 0 \\\ -2 & 3 \\\ 4 & 1 \end{pmatrix}
$$

---

### 1. Sizes of Matrices $A$ and $B$

The size of a matrix is specified as $(\text{number of rows}) \times (\text{number of columns})$:

* Matrix $A$ has $2$ rows and $3$ columns, so its size is **$2 \times 3$**.
* Matrix $B$ has $3$ rows and $2$ columns, so its size is **$3 \times 2$**.

---

### 2. Matrix Entries

Using standard index notation $x_{ij}$ (row $i$, column $j$):

* $a_{12} = -1$ (Row $1$, Column $2$ of $A$)
* $a_{23} = 5$ (Row $2$, Column $3$ of $A$)
* $b_{21} = -2$ (Row $2$, Column $1$ of $B$)
* $b_{32} = 1$ (Row $3$, Column $2$ of $B$)

---

### 3. Row and Column Vectors

* **Second row of $A$ (as a row vector):**

$$
\mathbf{r}_2(A) = \begin{pmatrix} 0 & 4 & 5 \end{pmatrix}
$$

* **First column of $B$ (as a column vector):**

$$
\mathbf{c}_1(B) = \begin{pmatrix} 1 \\\ -2 \\\ 4 \end{pmatrix}
$$

---

### Conclusion

* **Sizes:** $A$ is $2 \times 3$ and $B$ is $3 \times 2$.
* **Entries:** $a_{12} = -1$, $a_{23} = 5$, $b_{21} = -2$, $b_{32} = 1$.
* **Vectors:** Second row of $A$ is $(0, 4, 5)$ and first column of $B$ is $(1, -2, 4)^T$.
