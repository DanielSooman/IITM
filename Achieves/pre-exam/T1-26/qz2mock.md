
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





<img width="911" height="195" alt="image" src="https://github.com/user-attachments/assets/b2d1bac7-a3df-4e85-988b-c2751be42b20" />





Let’s work through this step by step:

### 1. Compute the mean vector
\[
\bar{x} = \frac{x_1 + x_2 + x_3}{3}
= \frac{\begin{bmatrix}1 \\ 1\end{bmatrix} + \begin{bmatrix}2 \\ 3\end{bmatrix} + \begin{bmatrix}3 \\ 2\end{bmatrix}}{3}
= \frac{\begin{bmatrix}6 \\ 6\end{bmatrix}}{3}
= \begin{bmatrix}2 \\ 2\end{bmatrix}
\]

### 2. Compute deviations
\[
x_1 - \bar{x} = \begin{bmatrix}-1 \\ -1\end{bmatrix}, \quad
x_2 - \bar{x} = \begin{bmatrix}0 \\ 1\end{bmatrix}, \quad
x_3 - \bar{x} = \begin{bmatrix}1 \\ 0\end{bmatrix}
\]

### 3. Compute outer products
\[
(x_1 - \bar{x})(x_1 - \bar{x})^T = \begin{bmatrix}1 & 1 \\ 1 & 1\end{bmatrix}
\]
\[
(x_2 - \bar{x})(x_2 - \bar{x})^T = \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix}
\]
\[
(x_3 - \bar{x})(x_3 - \bar{x})^T = \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix}
\]

### 4. Sum them up
\[
\sum = \begin{bmatrix}1 & 1 \\ 1 & 1\end{bmatrix} + \begin{bmatrix}0 & 0 \\ 0 & 1\end{bmatrix} + \begin{bmatrix}1 & 0 \\ 0 & 0\end{bmatrix}
= \begin{bmatrix}2 & 1 \\ 1 & 2\end{bmatrix}
\]

### 5. Divide by \(n=3\)
\[
C = \frac{1}{3} \begin{bmatrix}2 & 1 \\ 1 & 2\end{bmatrix}
= \begin{bmatrix}\tfrac{2}{3} & \tfrac{1}{3} \\ \tfrac{1}{3} & \tfrac{2}{3}\end{bmatrix}
\]

### 6. Eigenvalues
For a \(2 \times 2\) matrix \(\begin{bmatrix}a & b \\ b & a\end{bmatrix}\), eigenvalues are \(a+b\) and \(a-b\).

Here \(a = \tfrac{2}{3}, b = \tfrac{1}{3}\):
\[
\lambda_1 = \tfrac{2}{3} + \tfrac{1}{3} = 1, \quad
\lambda_2 = \tfrac{2}{3} - \tfrac{1}{3} = \tfrac{1}{3}
\]

### 7. Sum of eigenvalues
\[
\lambda_1 + \lambda_2 = 1 + \tfrac{1}{3} = \tfrac{4}{3} \approx 1.33
\]

✅ **Final Answer: 1.33**
