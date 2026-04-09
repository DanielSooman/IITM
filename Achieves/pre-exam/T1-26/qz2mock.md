
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

To find the sum of the eigenvalues of the covariance matrix $C$, we can use a key property: **the sum of the eigenvalues of a matrix equals its trace**.

For the covariance matrix, the trace is also the total variance.

### Step 1: Find the mean vector $\overline{x_i}$

Given:
$$x_1 = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad x_2 = \begin{bmatrix} 2 \\ 3 \end{bmatrix}, \quad x_3 = \begin{bmatrix} 3 \\ 2 \end{bmatrix}$$

$$\overline{x_i} = \frac{x_1 + x_2 + x_3}{3} = \frac{1}{3}\begin{bmatrix} 1+2+3 \\ 1+3+2 \end{bmatrix} = \begin{bmatrix} 2 \\ 2 \end{bmatrix}$$

### Step 2: Compute $C$ using the formula

$$C = \frac{1}{n} \sum_{i=1}^{n}(x_i - \overline{x_i})(x_i - \overline{x_i})^T$$

First, find each deviation:
$$x_1 - \overline{x_i} = \begin{bmatrix} 1-2 \\ 1-2 \end{bmatrix} = \begin{bmatrix} -1 \\ -1 \end{bmatrix}$$
$$x_2 - \overline{x_i} = \begin{bmatrix} 2-2 \\ 3-2 \end{bmatrix} = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$$
$$x_3 - \overline{x_i} = \begin{bmatrix} 3-2 \\ 2-2 \end{bmatrix} = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$$

Now compute each outer product:

$$(x_1 - \overline{x_i})(x_1 - \overline{x_i})^T = \begin{bmatrix} -1 \\ -1 \end{bmatrix}\begin{bmatrix} -1 & -1 \end{bmatrix} = \begin{bmatrix} 1 & 1 \\ 1 & 1 \end{bmatrix}$$

$$(x_2 - \overline{x_i})(x_2 - \overline{x_i})^T = \begin{bmatrix} 0 \\ 1 \end{bmatrix}\begin{bmatrix} 0 & 1 \end{bmatrix} = \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix}$$

$$(x_3 - \overline{x_i})(x_3 - \overline{x_i})^T = \begin{bmatrix} 1 \\ 0 \end{bmatrix}\begin{bmatrix} 1 & 0 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$$

Sum them:
$$\sum = \begin{bmatrix} 1+0+1 & 1+0+0 \\ 1+0+0 & 1+1+0 \end{bmatrix} = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}$$

Then divide by $n = 3$:
$$C = \frac{1}{3}\begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix} = \begin{bmatrix} \frac{2}{3} & \frac{1}{3} \\ \frac{1}{3} & \frac{2}{3} \end{bmatrix}$$

### Step 3: Sum of eigenvalues = trace of $C$

$$\text{trace}(C) = \frac{2}{3} + \frac{2}{3} = \frac{4}{3} \approx 1.3333...$$

Rounded to two decimals: **1.33**

So the sum of the eigenvalues of the covariance matrix is 1.33.
### 7. Sum of eigenvalues
\[
\lambda_1 + \lambda_2 = 1 + \tfrac{1}{3} = \tfrac{4}{3} \approx 1.33
\]

✅ **Final Answer: 1.33**
