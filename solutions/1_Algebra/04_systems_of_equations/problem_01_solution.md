# Exercise 1. From a System to a Matrix

## Question

Write the system

$$
\begin{cases}
2x - y + z = 4, \\\
x + 3y - 2z = 1, \\\
3x + y + z = 7.
\end{cases}
$$

in the form $Ax = b$. Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

---

## Solution

We are given a $3 \times 3$ system of linear equations in the unknowns $x, y, z$:

$$
\begin{cases}
2x - y + z = 4, \\\
x + 3y - 2z = 1, \\\
3x + y + z = 7.
\end{cases}
$$

---

### 1. Write the System in the Matrix Form $Ax = b$

Collecting the coefficients of $x$, $y$, and $z$ into a $3 \times 3$ matrix $A$, the unknowns into a $3 \times 1$ column vector $x$, and the constants into a $3 \times 1$ column vector $b$, the system takes the form $Ax = b$:

$$
\begin{pmatrix} 2 & -1 & 1 \\\ 1 & 3 & -2 \\\ 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\\ y \\\ z \end{pmatrix} = \begin{pmatrix} 4 \\\ 1 \\\ 7 \end{pmatrix}
$$

---

### 2. Identify $A$, $x$, and $b$

* **Coefficient matrix ($A$):**

$$
A = \begin{pmatrix} 2 & -1 & 1 \\\ 1 & 3 & -2 \\\ 3 & 1 & 1 \end{pmatrix}
$$

* **Vector of unknowns ($x$):**

$$
x = \begin{pmatrix} x \\\ y \\\ z \end{pmatrix}
$$

* **Right-hand side vector ($b$):**

$$
b = \begin{pmatrix} 4 \\\ 1 \\\ 7 \end{pmatrix}
$$

---

### 3. How Each Row of the Matrix Corresponds to One Equation

By the definition of matrix–vector multiplication, the $i$-th entry of $Ax$ is obtained by taking the dot product of the $i$-th row of $A$ with the column vector of unknowns $x$, and setting it equal to the $i$-th entry of $b$:

1. **Row 1:** Multiplying the first row $(2, -1, 1)$ by $x$ gives $2(x) + (-1)(y) + 1(z) = 2x - y + z$, which equals the first entry of $b$ ($4$), reproducing the first equation **$2x - y + z = 4$**.
2. **Row 2:** Multiplying the second row $(1, 3, -2)$ by $x$ gives $1(x) + 3(y) + (-2)(z) = x + 3y - 2z$, which equals the second entry of $b$ ($1$), reproducing the second equation **$x + 3y - 2z = 1$**.
3. **Row 3:** Multiplying the third row $(3, 1, 1)$ by $x$ gives $3(x) + 1(y) + 1(z) = 3x + y + z$, which equals the third entry of $b$ ($7$), reproducing the third equation **$3x + y + z = 7$**.

---

### Conclusion

* **Matrix form ($Ax = b$):**

$$
\begin{pmatrix} 2 & -1 & 1 \\\ 1 & 3 & -2 \\\ 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\\ y \\\ z \end{pmatrix} = \begin{pmatrix} 4 \\\ 1 \\\ 7 \end{pmatrix}
$$

* Each row of $A$ stores the ordered coefficients of $(x, y, z)$ for a single equation, while the corresponding entry of $b$ stores that equation's constant term.
