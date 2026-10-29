# Exercise 3. When Can Matrices Be Multiplied?

**Given Matrix Dimensions:**
- $A$ is of size $2 \times 3$
- $B$ is of size $3 \times 4$
- $C$ is of size $4 \times 2$
- $D$ is of size $2 \times 2$

---

### **Dimension Compatibility Condition**
The matrix product $XY$ is defined if and only if the number of columns in the first matrix ($X$) equals the number of rows in the second matrix ($Y$):

$$
(m \times k) \cdot (k \times n) \implies (m \times n)
$$

---

### **Evaluation of Each Product**

* **$AB$:**
  * Dimensions: $(2 \times 3) \cdot (3 \times 4)$
  * **Defined:** Yes ($3 = 3$)
  * **Resulting Size:** $2 \times 4$

* **$BA$:**
  * Dimensions: $(3 \times 4) \cdot (2 \times 3)$
  * **Defined:** No ($4 \neq 2$)
  * **Resulting Size:** Undefined

* **$BC$:**
  * Dimensions: $(3 \times 4) \cdot (4 \times 2)$
  * **Defined:** Yes ($4 = 4$)
  * **Resulting Size:** $3 \times 2$

* **$CB$:**
  * Dimensions: $(4 \times 2) \cdot (3 \times 4)$
  * **Defined:** No ($2 \neq 3$)
  * **Resulting Size:** Undefined

* **$AC$:**
  * Dimensions: $(2 \times 3) \cdot (4 \times 2)$
  * **Defined:** No ($3 \neq 4$)
  * **Resulting Size:** Undefined

* **$CA$:**
  * Dimensions: $(4 \times 2) \cdot (2 \times 3)$
  * **Defined:** Yes ($2 = 2$)
  * **Resulting Size:** $4 \times 3$

* **$AD$:**
  * Dimensions: $(2 \times 3) \cdot (2 \times 2)$
  * **Defined:** No ($3 \neq 2$)
  * **Resulting Size:** Undefined

* **$DA$:**
  * Dimensions: $(2 \times 2) \cdot (2 \times 3)$
  * **Defined:** Yes ($2 = 2$)
  * **Resulting Size:** $2 \times 3$
