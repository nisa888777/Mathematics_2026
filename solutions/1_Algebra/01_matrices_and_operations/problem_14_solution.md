# Exercise 14. Rotation Matrices

**Given Rotation Matrix:**

$$
R(\theta) = \begin{pmatrix} \cos\theta & -\sin\theta \\\ \sin\theta & \cos\theta \end{pmatrix}
$$

---

### **1. Compute the Product $R(\alpha)R(\beta)$**

Writing the rotation matrices for angles $\alpha$ and $\beta$:

$$
R(\alpha) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\\ \sin\alpha & \cos\alpha \end{pmatrix}, \quad R(\beta) = \begin{pmatrix} \cos\beta & -\sin\beta \\\ \sin\beta & \cos\beta \end{pmatrix}
$$

Performing matrix multiplication:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha & -\sin\alpha \\\ \sin\alpha & \cos\alpha \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\\ \sin\beta & \cos\beta \end{pmatrix}
$$

Evaluating each entry by multiplying rows of $R(\alpha)$ by columns of $R(\beta)$:

* **Row 1, Column 1:**  
  $$(\cos\alpha)(\cos\beta) + (-\sin\alpha)(\sin\beta) = \cos\alpha \cos\beta - \sin\alpha \sin\beta$$

* **Row 1, Column 2:**  
  $$(\cos\alpha)(-\sin\beta) + (-\sin\alpha)(\cos\beta) = -(\sin\alpha \cos\beta + \cos\alpha \sin\beta)$$

* **Row 2, Column 1:**  
  $$(\sin\alpha)(\cos\beta) + (\cos\alpha)(\sin\beta) = \sin\alpha \cos\beta + \cos\alpha \sin\beta$$

* **Row 2, Column 2:**  
  $$(\sin\alpha)(-\sin\beta) + (\cos\alpha)(\cos\beta) = \cos\alpha \cos\beta - \sin\alpha \sin\beta$$

Putting these entries together:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos\alpha \cos\beta - \sin\alpha \sin\beta & -(\sin\alpha \cos\beta + \cos\alpha \sin\beta) \\\ \sin\alpha \cos\beta + \cos\alpha \sin\beta & \cos\alpha \cos\beta - \sin\alpha \sin\beta \end{pmatrix}
$$

---

### **2. Apply Angle-Sum Formulas**

Using the standard trigonometric sum formulas:

* For cosine:
  $$\cos(\alpha + \beta) = \cos\alpha \cos\beta - \sin\alpha \sin\beta$$

* For sine:
  $$\sin(\alpha + \beta) = \sin\alpha \cos\beta + \cos\alpha \sin\beta$$

Substituting these identities directly into the product matrix:

$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha + \beta) & -\sin(\alpha + \beta) \\\ \sin(\alpha + \beta) & \cos(\alpha + \beta) \end{pmatrix} = R(\alpha + \beta)
$$

This proves that:

$$
R(\alpha)R(\beta) = R(\alpha + \beta)
$$

---

### **3. Geometric Explanation**

* **Transformation Composition:**  
  Multiplying a vector $\mathbf{x}$ by $R(\beta)$ rotates the vector counterclockwise about the origin by an angle $\beta$. Multiplying the resulting vector by $R(\alpha)$ subsequently rotates it counterclockwise by an additional angle $\alpha$.
* **Net Effect:**  
  Successively rotating a vector in the plane first by $\beta$ and then by $\alpha$ about the same center is geometrically identical to performing a single rotation through the total accumulated angle $\alpha + \beta$.
* **Commutativity of 2D Rotations:**  
  Since scalar addition is commutative ($\alpha + \beta = \beta + \alpha$), it also follows that:

$$
R(\alpha)R(\beta) = R(\alpha + \beta) = R(\beta + \alpha) = R(\beta)R(\alpha)
$$

showing that rotations in the two-dimensional plane commute with each other.
