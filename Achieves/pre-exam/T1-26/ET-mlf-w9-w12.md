<details>
  <summary>Week9</summary>

<img width="923" height="429" alt="image" src="https://github.com/user-attachments/assets/c9fc62f0-0c7f-455c-bfec-3e31285bcdd5" />
<img width="1178" height="470" alt="image" src="https://github.com/user-attachments/assets/f1a5fd27-65ef-4492-a75b-2338a0f8651b" />
<img width="608" height="441" alt="image" src="https://github.com/user-attachments/assets/fe1f59a9-ceac-4646-8a89-586f23679fc0" />
<img width="739" height="444" alt="image" src="https://github.com/user-attachments/assets/accfa960-53d9-432e-9521-1971c5968fe9" />
  <details>
  <summary>Sol</summary>
  ## Solution

For a function f(x, y) to be **convex**, the **Hessian matrix must be positive semi-definite**.

### Step 1: Find the Hessian

Let f(x, y) = (x − 3)³ + (y + 1)²

**Partial derivatives:**
- f_x = 3(x − 3)²
- f_y = 2(y + 1)

**Second partial derivatives:**
- f_xx = 6(x − 3)
- f_yy = 2
- f_xy = 0

### Step 2: Hessian Matrix

$$H = \begin{bmatrix} 6(x-3) & 0 \\ 0 & 2 \end{bmatrix}$$

### Step 3: Positive Semi-Definite Conditions

For H to be positive semi-definite, **all leading principal minors must be ≥ 0**:

- **H₁₁ ≥ 0:** 6(x − 3) ≥ 0 → **x ≥ 3**
- **det(H) ≥ 0:** 6(x − 3) · 2 ≥ 0 → x ≥ 3 ✓

### Conclusion

The function is convex when **x ≥ 3**.

> ✅ **Answer: x ≥ 3**

  </details>
<img width="1044" height="425" alt="image" src="https://github.com/user-attachments/assets/1a51fc10-339f-45d6-9171-7d5006418214" />
  <details>
  <summary>Sol-5</summary>
    
  ## Linear Approximation

The linear approximation formula is:
$$f(x_0 + \Delta x, y_0 + \Delta y) \approx f(x_0, y_0) + f_x(x_0,y_0)\Delta x + f_y(x_0,y_0)\Delta y$$

**Step 1: Find the partial derivatives**
$$f_x = 2x, \quad f_y = 2y$$

**Step 2: Evaluate at point (3, 2)**
$$f(3,2) = 3^2 + 2^2 = 9 + 4 = 13$$
$$f_x(3,2) = 2(3) = 6, \quad f_y(3,2) = 2(2) = 4$$

**Step 3: Find the step in direction (1, 2)**

First, normalize the direction vector (1, 2):
$$\|\mathbf{u}\| = \sqrt{1^2 + 2^2} = \sqrt{5}$$

The unit vector: $\hat{u} = \left(\dfrac{1}{\sqrt5}, \dfrac{2}{\sqrt5}\right)$

With step size 0.02:
$$\Delta x = 0.02 \cdot \frac{1}{\sqrt{5}}, \quad \Delta y = 0.02 \cdot \frac{2}{\sqrt{5}}$$

**Step 4: Apply the formula**
$$f \approx 13 + 6\cdot\frac{0.02}{\sqrt5} + 4\cdot\frac{0.04}{\sqrt5}$$
$$= 13 + \frac{0.12 + 0.16}{\sqrt5} = 13 + \frac{0.28}{\sqrt5}$$
$$= 13 + \frac{0.28}{2.2361} \approx 13 + 0.1252 \approx \mathbf{13.13}$$

Hmm — but if the direction (1,2) is used **without normalizing** (treating Δx = 0.02·1, Δy = 0.02·2):
$$f \approx 13 + 6(0.02) + 4(0.04) = 13 + 0.12 + 0.16 = \mathbf{13.28}$$

This matches option **13.28**, and the question likely intends the direction vector to be used directly (scaled by 0.02).

### ✅ Answer: **13.28**

  </details>

</details>











<img width="922" height="327" alt="image" src="https://github.com/user-attachments/assets/3ef5ace2-b311-4a9e-9e78-d2d1bddcae26" />

  <details>
  <summary>Sol</summary>

  ## Solution

**Minimize** f(x, y) = x² + 4y² − 2x + 8y **subject to** x + 2y = 7

### Step 1: Use the Constraint

From x + 2y = 7, express x = 7 − 2y

### Step 2: Substitute into f

f = (7 − 2y)² + 4y² − 2(7 − 2y) + 8y

= 49 − 28y + 4y² + 4y² − 14 + 4y + 8y

= **8y² − 16y + 35**

### Step 3: Minimize the Single-Variable Function

f(y) = 8y² − 16y + 35

f'(y) = 16y − 16 = 0

**y = 1**

### Step 4: Find x

x = 7 − 2(1) = **5**

### Step 5: Compute Minimum Value

f(5, 1) = 25 + 4(1) − 10 + 8 = 25 + 4 − 10 + 8 = **27**

> The minimum value is **27.00**, which falls within the accepted range [26.50, 27.50] ✓

  </details>
