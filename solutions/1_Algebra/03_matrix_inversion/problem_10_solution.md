# Exercise 10. Inverse of a Diagonal Matrix

## Question

Given

$$
D = \begin{pmatrix} 2 & 0 & 0 \\\ 0 & -3 & 0 \\\ 0 & 0 & 5 \end{pmatrix}, \qquad E = \begin{pmatrix} 2 & 0 & 0 \\\ 0 & 0 & 0 \\\ 0 & 0 & 5 \end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

---

## Solution

We are given two $3 \times 3$ diagonal matrices:

$$
D = \begin{pmatrix} 2 & 0 & 0 \\\ 0 & -3 & 0 \\\ 0 & 0 & 5 \end{pmatrix}, \qquad E = \begin{pmatrix} 2 & 0 & 0 \\\ 0 & 0 & 0 \\\ 0 & 0 & 5 \end{pmatrix}
$$

---

### 1. Decide Which Matrix Is Invertible

A diagonal matrix is invertible if and only if **all of its main diagonal entries are non-zero** (equivalently, its determinant, which is the product of its diagonal entries, is non-zero).

* **For matrix $D$:** The diagonal entries are $2$, $-3$, and $5$. Since none of them is zero ($\det(D) = 2 \cdot (-3) \cdot 5 = -30 \neq 0$), **$D$ is invertible**.
* **For matrix $E$:** The second diagonal entry is $0$ (creating an entire row and column of zeros, so $\det(E) = 2 \cdot 0 \cdot 5 = 0$). Therefore, **$E$ is singular (not invertible)**.

---

### 2. Find the Inverse of $D$

For any invertible diagonal matrix, the inverse is obtained directly by taking the reciprocal of each main diagonal entry:

$$
D^{-1} = \begin{pmatrix} \frac{1}{2} & 0 & 0 \\\ 0 & -\frac{1}{3} & 0 \\\ 0 & 0 & \frac{1}{5} \end{pmatrix}
$$

---

### 3. Check the Result by Multiplication

We verify that $D D^{-1} = I$:

$$
D D^{-1} = \begin{pmatrix} 2 & 0 & 0 \\\ 0 & -3 & 0 \\\ 0 & 0 & 5 \end{pmatrix} \begin{pmatrix} \frac{1}{2} & 0 & 0 \\\ 0 & -\frac{1}{3} & 0 \\\ 0 & 0 & \frac{1}{5} \end{pmatrix} = \begin{pmatrix} 2\left(\frac{1}{2}\right) & 0 & 0 \\\ 0 & (-3)\left(-\frac{1}{3}\right) & 0 \\\ 0 & 0 & 5\left(\frac{1}{5}\right) \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\\ 0 & 1 & 0 \\\ 0 & 0 & 1 \end{pmatrix} = I
$$

Similarly, $D^{-1} D = I$ holds because diagonal matrices commute. Thus, the inverse matrix is verified.

---

### Conclusion

* **Invertibility:** $D$ is invertible because all its diagonal entries are non-zero, whereas $E$ is not invertible due to the zero entry on its diagonal.
* **Inverse matrix:**

$$
D^{-1} = \begin{pmatrix} \frac{1}{2} & 0 & 0 \\\ 0 & -\frac{1}{3} & 0 \\\ 0 & 0 & \frac{1}{5} \end{pmatrix}
$$
