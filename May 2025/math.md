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
