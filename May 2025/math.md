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


