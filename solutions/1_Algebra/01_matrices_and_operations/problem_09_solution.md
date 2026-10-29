# Exercise 9. Composing Transformations

**Given:**

$$
S = \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix}, \quad R = \begin{pmatrix} 0 & -1 \\\ 1 & 0 \end{pmatrix}, \quad \mathbf{x} = \begin{pmatrix} 1 \\\ 2 \end{pmatrix}
$$

* Matrix $S$ represents nonuniform scaling (stretches along the $x$-axis by a factor of $2$).
* Matrix $R$ represents a $90^\circ$ counterclockwise rotation.

---

### **1. Compute $RS\mathbf{x}$**

In this composition, scaling $S$ is applied first, followed by rotation $R$.

* **Step 1: Compute $S\mathbf{x}$**

$$
S\mathbf{x} = \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\\ 2 \end{pmatrix} = \begin{pmatrix} (2)(1) + (0)(2) \\\ (0)(1) + (1)(2) \end{pmatrix} = \begin{pmatrix} 2 \\\ 2 \end{pmatrix}
$$

* **Step 2: Apply $R$ to $S\mathbf{x}$**

$$
RS\mathbf{x} = R(S\mathbf{x}) = \begin{pmatrix} 0 & -1 \\\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\\ 2 \end{pmatrix} = \begin{pmatrix} (0)(2) + (-1)(2) \\\ (1)(2) + (0)(2) \end{pmatrix} = \begin{pmatrix} -2 \\\ 2 \end{pmatrix}
$$

---

### **2. Compute $SR\mathbf{x}$**

In this composition, rotation $R$ is applied first, followed by scaling $S$.

* **Step 1: Compute $R\mathbf{x}$**

$$
R\mathbf{x} = \begin{pmatrix} 0 & -1 \\\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\\ 2 \end{pmatrix} = \begin{pmatrix} (0)(1) + (-1)(2) \\\ (1)(1) + (0)(2) \end{pmatrix} = \begin{pmatrix} -2 \\\ 1 \end{pmatrix}
$$

* **Step 2: Apply $S$ to $R\mathbf{x}$**

$$
SR\mathbf{x} = S(R\mathbf{x}) = \begin{pmatrix} 2 & 0 \\\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\\ 1 \end{pmatrix} = \begin{pmatrix} (2)(-2) + (0)(1) \\\ (0)(-2) + (1)(1) \end{pmatrix} = \begin{pmatrix} -4 \\\ 1 \end{pmatrix}
$$

---

### **3. Comparison of Results**

$$
RS\mathbf{x} = \begin{pmatrix} -2 \\\ 2 \end{pmatrix} \neq \begin{pmatrix} -4 \\\ 1 \end{pmatrix} = SR\mathbf{x}
$$

---

### **4. Geometric Explanation**

The order of transformations matters because matrix multiplication corresponds to function composition, which is generally noncommutative:

* **For $RS\mathbf{x}$ (Scale then Rotate):**  
  The vector $\mathbf{x} = (1, 2)^T$ is first scaled horizontally, doubling its $x$-coordinate to become $(2, 2)^T$. Rotating this by $90^\circ$ counterclockwise swings that stretched $x$-component into the negative $y$-direction, landing at $(-2, 2)^T$.

* **For $SR\mathbf{x}$ (Rotate then Scale):**  
  The vector $\mathbf{x} = (1, 2)^T$ is first rotated by $90^\circ$ counterclockwise to $(-2, 1)^T$. When nonuniform scaling is applied afterward, it scales the *new* $x$-coordinate (which was originally the vertical component), doubling it to $-4$ and resulting in $(-4, 1)^T$.

Since scaling stretches only along the fixed horizontal axis, stretching an axis before or after rotating the coordinate frame alters which directional component gets doubled.
