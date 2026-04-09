
<img width="1045" height="45" alt="image" src="https://github.com/user-attachments/assets/c81f467c-246e-4997-890b-73e87e7e6f66" />

To find the second-order approximate value of $f(10)$, we use the **Taylor series expansion** centered at $a = 20$.

The second-order Taylor polynomial $P_2(x)$ for a function $f(x)$ at $x=a$ is given by:

$$f(x) \approx f(a) + f'(a)(x - a) + \frac{f''(a)}{2!}(x - a)^2$$

### 1. Identify the given values
From your problem statement, we have:
* Center point $a = 20$
* Target point $x = 10$
* $f(20) = 1$
* $f'(20) = 10$
* $f''(20) = 5$

### 2. Calculate the difference $(x - a)$
$$\Delta x = x - a = 10 - 20 = -10$$

### 3. Substitute into the Taylor formula
$$f(10) \approx 1 + 10(10 - 20) + \frac{5}{2}(10 - 20)^2$$

$$f(10) \approx 1 + 10(-10) + \frac{5}{2}(-10)^2$$

$$f(10) \approx 1 - 100 + \frac{5}{2}(100)$$

$$f(10) \approx 1 - 100 + 250$$

$$f(10) \approx 151$$

---

**Final Answer:**
The second order approximate value of $f(10)$ is **151**.






