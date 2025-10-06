<img width="1027" height="560" alt="image" src="https://github.com/user-attachments/assets/95cecaee-5cf4-497f-8602-1d9bee34127a" />
<img width="319" height="91" alt="image" src="https://github.com/user-attachments/assets/43bbf3ca-f08f-4e3c-b4d0-d60ba35f1114" />


We are given four functions defined on $ \mathbb{R}^2 \setminus \{(0,0)\} $, and we are to determine **for which of them the limit exists at $ (0,0) $**.

Let’s analyze each function one by one.

---

### **Function 1:**
$$
f_1(x,y) = 1 - e^{-\frac{1}{x^2 + y^2}}
$$

Let $ r^2 = x^2 + y^2 $. As $ (x,y) \to (0,0) $, $ r \to 0^+ $, so $ \frac{1}{r^2} \to \infty $, and thus:
$$
e^{-\frac{1}{r^2}} \to e^{-\infty} = 0
$$
So:
$$
f_1(x,y) \to 1 - 0 = 1
$$

✅ **Limit exists and equals 1.**

✔️ So **$ f_1 $** has a limit at $ (0,0) $.

---

### **Function 2:**
$$
f_2(x,y) = 1 - e^{\frac{1}{x^2 + y^2}}
$$

Again, let $ r^2 = x^2 + y^2 $. As $ r \to 0^+ $, $ \frac{1}{r^2} \to \infty $, so:
$$
e^{\frac{1}{r^2}} \to \infty \Rightarrow f_2(x,y) = 1 - \infty \to -\infty
$$

So the function goes to $ -\infty $ as $ (x,y) \to (0,0) $. But **the limit does not exist in the finite sense** (it diverges to $ -\infty $).

❌ **Limit does not exist (diverges).**

---

### **Function 3:**
$$
f_3(x,y) = \frac{1}{1 - e^{x^2 + y^2}}
$$

As $ (x,y) \to (0,0) $, $ x^2 + y^2 \to 0 $, so $ e^{x^2 + y^2} \to e^0 = 1 $

Thus:
$$
1 - e^{x^2 + y^2} \to 1 - 1 = 0
$$

But we need to check the sign:

Since $ x^2 + y^2 > 0 $ near $ (0,0) $, $ e^{x^2 + y^2} > 1 $, so $ 1 - e^{x^2 + y^2} < 0 $

So denominator approaches $ 0^- $, and numerator is 1, so:
$$
f_3(x,y) \to \frac{1}{0^-} = -\infty
$$

So again, it diverges to $ -\infty $, so **limit does not exist**.

❌ **Limit does not exist.**

---

### **Function 4:**
$$
f_4(x,y) = \frac{1}{1 + e^{x^2 + y^2}}
$$

As $ (x,y) \to (0,0) $, $ x^2 + y^2 \to 0 $, so $ e^{x^2 + y^2} \to 1 $

Thus:
$$
f_4(x,y) \to \frac{1}{1 + 1} = \frac{1}{2}
$$

✅ **Limit exists and equals $ \frac{1}{2} $.**

✔️ So **$ f_4 $** has a limit at $ (0,0) $.

---

### ✅ Final Answer:

The functions for which the limit exists at $ (0,0) $ are:

- $ f_1(x,y) $
- $ f_4(x,y) $

These are the ones marked with green boxes.

---

### ✅ Correct Options:
$$
\boxed{f_1(x,y) \quad \text{and} \quad f_4(x,y)}
$$


<img width="1032" height="438" alt="image" src="https://github.com/user-attachments/assets/8b729ca2-f800-44a3-9b73-720074d6c6fc" />
To find the direction of the steepest descent for the skier, you need to determine the negative of the gradient of the mountain's surface at the given point. The mountain's surface is described by the equation $z = f(x, y) = 20 - 0.4x^2 - 0.3y^2$. The gradient of this function, $\nabla f$, points in the direction of the greatest rate of increase, or the **steepest ascent**. Therefore, the direction of the **steepest descent** is in the opposite direction, which is given by $-\nabla f$.

The gradient of a function $f(x, y)$ is a vector of its partial derivatives:
$\nabla f = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right)$

First, calculate the partial derivatives of $f(x, y)$:
* $\frac{\partial f}{\partial x} = \frac{\partial}{\partial x}(20 - 0.4x^2 - 0.3y^2) = -0.8x$
* $\frac{\partial f}{\partial y} = \frac{\partial}{\partial y}(20 - 0.4x^2 - 0.3y^2) = -0.6y$

So, the gradient is $\nabla f = \langle -0.8x, -0.6y \rangle$.

Next, evaluate the gradient at the skier's location, which is the point $(1, -1)$:
* $\frac{\partial f}{\partial x}\bigg|_{(1, -1)} = -0.8(1) = -0.8$
* $\frac{\partial f}{\partial y}\bigg|_{(1, -1)} = -0.6(-1) = 0.6$

The gradient vector at this point is $\nabla f(1, -1) = \langle -0.8, 0.6 \rangle$. This vector points in the direction of the steepest ascent.

Finally, to find the direction of the steepest descent, take the negative of the gradient:
$-\nabla f(1, -1) = -\langle -0.8, 0.6 \rangle = \langle 0.8, -0.6 \rangle$

The skier should begin skiing in the direction of the vector $\langle 0.8, -0.6 \rangle$. This corresponds to the option **(0.8, -0.6)**.
<img width="1081" height="418" alt="image" src="https://github.com/user-attachments/assets/bf3407f8-1493-4835-b1c2-179e2078f071" />


Based on the image you uploaded, let's analyze each statement about the properties of determinants for an $n \times n$ matrix $A$.

---

### **Analyzing the Statements**

1.  **Let $\det(A) \neq 0$. Then the determinant of $A$ is unaltered by swapping any two rows of $A$.**
    This statement is **false**. A fundamental property of determinants is that swapping any two rows of a matrix *multiplies the determinant by -1*. This means the sign of the determinant changes.

2.  **The determinant of $A$ is unaltered when a multiple of a row is added to another row.**
    This statement is **true**. This is a key property used in Gaussian elimination to simplify matrices for calculating determinants. Adding a multiple of one row to another row (a type of elementary row operation) does not change the determinant.

3.  **For any real number $t$, $\det(tA) = t^n \det(A)$.**
    This statement is **true**. When you multiply a matrix $A$ by a scalar $t$, every row is multiplied by $t$. Since there are $n$ rows in an $n \times n$ matrix, and each row multiplication by $t$ scales the determinant by $t$, the total effect is scaling the determinant by $t \times t \times \dots \times t$ ($n$ times), which is $t^n$.

4.  **If $D = P^{-1}AP$, then $D = A$.**
    This statement is **false**. The equation $D = P^{-1}AP$ describes a **similarity transformation**, which means that matrices $A$ and $D$ are similar. Similar matrices have many properties in common, such as the same determinant, trace, eigenvalues, and characteristic polynomial. However, they are **not necessarily equal**. The equation $D=A$ would only hold true in specific cases, for example, if $P$ is the identity matrix ($I$), or if $A$ is a multiple of the identity matrix.

---

### **Conclusion**

The correct statements are:
* **Determinant of $A$ is unaltered when a multiple of a row is added to another row.**
* **For any real number $t$, $\det(tA) = t^n \det(A)$.**

Your image correctly identifies these two statements.

