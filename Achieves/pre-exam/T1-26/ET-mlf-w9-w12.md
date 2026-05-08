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














<img width="751" height="325" alt="image" src="https://github.com/user-attachments/assets/58b2a839-cfb4-43e3-8197-0d7213f6947a" />



  <details>
  <summary>Sol</summary>

  ## Distance of a Plane from the Origin

The formula for the distance from the origin to the plane **ax + by + cz = d** is:

$$D = \frac{|d|}{\sqrt{a^2 + b^2 + c^2}}$$

### Applying to x + y − 2z = 6

Here: a = 1, b = 1, c = −2, d = 6

$$D = \frac{|6|}{\sqrt{1^2 + 1^2 + (-2)^2}}$$

$$D = \frac{6}{\sqrt{1 + 1 + 4}} = \frac{6}{\sqrt{6}}$$

$$D = \frac{6}{\sqrt{6}} = \frac{6\sqrt{6}}{6} = \sqrt{6}$$

$$\boxed{D = \sqrt{6} \approx 2.449...  \approx 2.45}$$

### Why the accepted range is 2.30 – 2.60

√6 ≈ 2.449, which falls within the accepted range of **2.30 to 2.60**. The answer **2.39** was also accepted as it lies within that range (likely a rounding/approximation was used).

The **exact answer is √6 ≈ 2.45**.

  </details>

















<img width="1100" height="321" alt="image" src="https://github.com/user-attachments/assets/8ac2d511-4c4f-4004-909f-88e076d5aeeb" />

  <details>
  <summary>Sol</summary>
## Solution

**Problem:** Find the maximum volume of a cuboid made from cardboard with total surface area = 24 cm².

### Setup

For a cuboid with dimensions *a*, *b*, *c*:
- **Surface area:** 2(ab + bc + ca) = 24 → ab + bc + ca = 12
- **Volume:** V = abc

### Optimization using AM-GM Inequality

By the **AM-GM inequality**:

$$\frac{ab + bc + ca}{3} \geq (a^2b^2c^2)^{1/3}$$

$$\frac{12}{3} \geq (abc)^{2/3}$$

$$4 \geq V^{2/3}$$

$$V \leq 4^{3/2} = 8$$

### When does equality hold?

Equality in AM-GM holds when **ab = bc = ca**, which means **a = b = c** (a cube).

If a = b = c, then:
$$2(3a^2) = 24 \implies a^2 = 4 \implies a = 2 \text{ cm}$$

### Maximum Volume

$$V = a^3 = 2^3 = \boxed{8 \text{ cm}^3}$$

---

> **Note:** The accepted range is 7.50–8.50, and the answer 8.10 was marked correct. The **exact theoretical maximum is 8.00 cm³**, achieved when the box is a perfect cube of side 2 cm.
  </details>






<img width="1371" height="485" alt="image" src="https://github.com/user-attachments/assets/ed08d087-ae06-4e8d-9121-10106d041f7f" />


  <details>
  <summary>Sol</summary>
  # Lagrange Multiplier Optimization

## Problem Setup

**Maximize:** r = l·m² + 2c

**Subject to:** b = 2l + 16m + c = 1004

## Using Lagrange Multipliers

∇r = λ∇b

Taking partial derivatives:

**∂r/∂l = m²** = λ·2 → **λ = m²/2**

**∂r/∂m = 2lm** = λ·16 → **λ = 2lm/16 = lm/8**

**∂r/∂c = 2** = λ·1 → **λ = 2**

## Solving the System

From λ = 2:

**From ∂r/∂l:** m² = 2·2 = 4 → **m = 2**

**From ∂r/∂m:** lm/8 = 2 → l·2/8 = 2 → **l = 8**

**From constraint:** 2(8) + 16(2) + c = 1004
→ 16 + 32 + c = 1004
→ **c = 956**

## Maximum Revenue

r = l·m² + 2c = 8·(2²) + 2·(956)

r = 8·4 + 1912

r = 32 + 1912

## **r = 1944 million rupees ✓**

The answer is **1944**, confirmed by the Lagrange multiplier method where λ = 2 gives us the optimal allocation of l = 8, m = 2, c = 956.

  </details>




<img width="846" height="306" alt="image" src="https://github.com/user-attachments/assets/fc4159e6-767d-4006-8179-387a21d45cb8" />






  <details>
  <summary>Sol</summary>
## Solution

**Find the point on the sphere x² + y² + z² = 3 closest to (2, 2, 2), then find the distance.**

**Step 1: Find the closest point on the sphere**

The closest point lies along the line from the origin (center of sphere) to the external point (2, 2, 2).

Direction vector from origin to (2, 2, 2):
$$\hat{u} = \frac{(2,2,2)}{|(2,2,2)|} = \frac{(2,2,2)}{\sqrt{4+4+4}} = \frac{(2,2,2)}{2\sqrt{3}}$$

**Step 2: Find the closest point on the sphere**

The sphere has radius √3, so the closest point is:
$$P = \sqrt{3} \cdot \hat{u} = \sqrt{3} \cdot \frac{(2,2,2)}{2\sqrt{3}} = \frac{(2,2,2)}{2} = (1, 1, 1)$$

**Step 3: Calculate the distance from (1,1,1) to (2,2,2)**

$$d = \sqrt{(2-1)^2 + (2-1)^2 + (2-1)^2} = \sqrt{1+1+1} = \sqrt{3}$$

$$\boxed{d = \sqrt{3} \approx 1.73}$$

**Alternative approach:** Distance from origin to (2,2,2) minus the radius:
$$d = 2\sqrt{3} - \sqrt{3} = \sqrt{3} \approx 1.73$$

Both methods confirm **√3 ≈ 1.73**, which falls within the accepted range of [1.50, 2.50] ✓
  </details>




<img width="932" height="312" alt="image" src="https://github.com/user-attachments/assets/181675c0-b548-4790-80dc-60f786677e37" />




  <details>
  <summary>Sol</summary>
    
## Solution

**Find the point on the sphere x² + y² + z² = 3 farthest from (2, 2, 2).**

**Key Insight:** The farthest point lies in the **opposite direction** from the external point, through the center (origin).

**Step 1: Direction from origin to (2,2,2)**

$$\hat{u} = \frac{(2,2,2)}{2\sqrt{3}}$$

**Step 2: Farthest point is in the opposite direction**

$$P = -\sqrt{3} \cdot \hat{u} = -\sqrt{3} \cdot \frac{(2,2,2)}{2\sqrt{3}} = \frac{-(2,2,2)}{2} = (-1, -1, -1)$$

**Step 3: Distance from (-1,-1,-1) to (2,2,2)**

$$d = \sqrt{(2-(-1))^2 + (2-(-1))^2 + (2-(-1))^2}$$

$$d = \sqrt{3^2 + 3^2 + 3^2} = \sqrt{27} = 3\sqrt{3}$$

$$\boxed{d = 3\sqrt{3} \approx 5.196}$$

**Alternative approach:** Distance from origin to (2,2,2) **plus** the radius:
$$d = 2\sqrt{3} + \sqrt{3} = 3\sqrt{3} \approx 5.196$$

This falls within the accepted range [5.00, 6.00] ✓

> Notice Q12 and Q13 are **mirror problems** — same sphere, same point, just closest vs farthest, giving **√3** and **3√3** respectively.
  </details>





</details>







---
















<details>
  <summary>Week10</summary>
<img width="753" height="347" alt="image" src="https://github.com/user-attachments/assets/38866c1d-4879-479f-958f-fe10bd348de8" />


  <details>
  <summary>Sol</summary>

    
## Solution

To determine if f(x) = xe^(-3x) is increasing or decreasing at x = 2, we need to find **f'(x)** and evaluate its sign.

### Step 1: Find f'(x)

Using the **Product Rule**: (uv)' = u'v + uv'

Let u = x and v = e^(-3x)

$$f'(x) = (1) \cdot e^{-3x} + x \cdot (-3e^{-3x})$$

$$f'(x) = e^{-3x}(1 - 3x)$$

### Step 2: Evaluate f'(2)

$$f'(2) = e^{-3(2)}(1 - 3(2))$$

$$f'(2) = e^{-6}(1 - 6)$$

$$f'(2) = -5e^{-6}$$

### Step 3: Interpret the Sign

Since e^(-6) > 0 always, and multiplied by **-5**:

$$f'(2) = -5e^{-6} < 0$$

### Conclusion

Since f'(2) < 0, the function is **decreasing** at x = 2. ✓
  </details>


<img width="708" height="283" alt="image" src="https://github.com/user-attachments/assets/69cdf964-c5b8-4640-b76d-bcc1fb10c517" />





  <details>
  <summary>Sol</summary>

# Finding the Global Minimum of f(x) = x + 3x²

## Step 1: Find the Critical Point

Take the derivative and set it equal to zero:

$$f'(x) = 1 + 6x = 0$$

$$x = -\frac{1}{6}$$

## Step 2: Verify it's a Minimum

$$f''(x) = 6 > 0 \checkmark$$

Since f''(x) > 0, this is indeed a **minimum** (concave up).

## Step 3: Find the Function Value

$$f\left(-\frac{1}{6}\right) = \left(-\frac{1}{6}\right) + 3\left(-\frac{1}{6}\right)^2$$

$$= -\frac{1}{6} + 3 \cdot \frac{1}{36}$$

$$= -\frac{1}{6} + \frac{1}{12}$$

$$= -\frac{2}{12} + \frac{1}{12}$$

$$= -\frac{1}{12}$$

$$\boxed{f\left(-\frac{1}{6}\right) = -\frac{1}{12} \approx -0.0833}$$

This falls within the accepted range of **[-0.09, -0.08]** ✓
  </details>


<img width="729" height="422" alt="image" src="https://github.com/user-attachments/assets/b764e4c7-7269-4ee7-8234-07fb6e862c8a" />
<img width="1202" height="470" alt="image" src="https://github.com/user-attachments/assets/24f4a6c2-5a18-40a1-85c5-6af665da251c" />

  <details>
  <summary>Sol</summary>

## Solution

### Setting up h(x) = f(g(x))

Given:
- f(x) = sin(x) − 2x² + 1
- g(x) = eˣ
- h = f∘g, so **h(x) = f(g(x)) = sin(eˣ) − 2e²ˣ + 1**

---

### First Derivative h'(x)

$$h'(x) = \cos(e^x) \cdot e^x - 4e^{2x}$$

$$h'(x) = e^x[\cos(e^x) - 4e^x]$$

**At x = 5:**
- e⁵ ≈ 148.41
- cos(e⁵) is bounded in [−1, 1]
- So: cos(e⁵) − 4e⁵ ≈ (something ≤ 1) − 4(148.41) ≈ **very negative**

$$h'(5) = e^5[\cos(e^5) - 4e^5] < 0$$

✅ **h(x) is decreasing at x = 5**

---

### Second Derivative h''(x)

$$h''(x) = \frac{d}{dx}\left[e^x\cos(e^x) - 4e^{2x}\right]$$

$$h''(x) = e^x\cos(e^x) - e^{2x}\sin(e^x) - 8e^{2x}$$

**At x = 5:**
- The dominant term is **−8e²ˣ** which is **hugely negative**
- sin(e⁵) is bounded, so −e¹⁰·sin(e⁵) could go either way but is swamped by −8e¹⁰

$$h''(5) \approx e^{10}[\text{bounded}] - 8e^{10} \ll 0$$

✅ **h''(5) < 0 → h(x) is concave at x = 5**

---

### Summary

| Statement | Verdict |
|-----------|---------|
| h(x) is convex | ❌ |
| **h(x) is concave** | ✅ |
| h(x) is non-decreasing | ❌ |
| **h(x) is decreasing** | ✅ |

  </details>















  <img width="1194" height="277" alt="image" src="https://github.com/user-attachments/assets/af7b974a-9c21-4747-8cc8-d9bd18612c4a" />


<img width="1403" height="606" alt="image" src="https://github.com/user-attachments/assets/476e6f71-931c-4bf1-a4f0-03f72f73ba8b" />


<img width="1373" height="442" alt="image" src="https://github.com/user-attachments/assets/f4bf051a-ffbf-425a-95ec-7e7c2645dc22" />





<img width="1343" height="701" alt="image" src="https://github.com/user-attachments/assets/0a8d2047-2cec-4a79-be09-3116d258ee8f" />


  <details>
  <summary>Sol</summary>


  ## Linear Regression Solution

The optimal weights are found using the **Normal Equation**:

$$w^* = (X^T X)^{-1} X^T y$$

### Setup

$$X = \begin{bmatrix} 1 & 2 \\ 2 & 3 \\ 4 & 2.5 \\ 6 & 4 \\ 7.5 & 5 \end{bmatrix}, \quad y = \begin{bmatrix} 1.5 \\ 2 \\ 2.5 \\ 3 \\ 4 \end{bmatrix}$$

### Step 1: Compute X^T X

$$X^T X = \begin{bmatrix} 1^2+2^2+4^2+6^2+7.5^2 & 1(2)+2(3)+4(2.5)+6(4)+7.5(5) \\ \cdot & 2^2+3^2+2.5^2+4^2+5^2 \end{bmatrix}$$

$$= \begin{bmatrix} 141.25 & 79.5 \\ 79.5 & 58.5 \end{bmatrix}$$

### Step 2: Compute X^T y

$$X^T y = \begin{bmatrix} 1(1.5)+2(2)+4(2.5)+6(3)+7.5(4) \\ 2(1.5)+3(2)+2.5(2.5)+4(3)+5(4) \end{bmatrix} = \begin{bmatrix} 78.5 \\ 54.5 \end{bmatrix}$$

### Step 3: Solve the System

Using the inverse of a 2×2 matrix with det = 141.25(58.5) − 79.5² = 8253.125 − 6320.25 = **1932.875**:

$$(X^T X)^{-1} = \frac{1}{1932.875}\begin{bmatrix} 58.5 & -79.5 \\ -79.5 & 141.25 \end{bmatrix}$$

$$w^* = (X^T X)^{-1} X^T y = \frac{1}{1932.875}\begin{bmatrix} 58.5(78.5) + (-79.5)(54.5) \\ (-79.5)(78.5) + 141.25(54.5) \end{bmatrix}$$

$$= \frac{1}{1932.875}\begin{bmatrix} 4592.25 - 4332.75 \\ -6240.75 + 7698.125 \end{bmatrix} = \frac{1}{1932.875}\begin{bmatrix} 259.5 \\ 1163.375 \end{bmatrix}$$

$$\boxed{w^* = \begin{bmatrix} 0.1382 \\ 0.6019 \end{bmatrix}}$$

  </details>






<img width="1416" height="452" alt="image" src="https://github.com/user-attachments/assets/1c423a34-fe57-464b-a7a1-9334db7b07cb" />



<details>
  <summary>Sol</summary>

  ## Solution Using Lagrangian Method

**Problem Setup:**
- Objective (maximize): R(s) = 100√s
- Constraint: 500s = 150,000 (budget constraint)

**Lagrangian Function:**

$$\mathcal{L}(s, \lambda) = 100\sqrt{s} - \lambda(500s - 150000)$$

**First-Order Conditions:**

$$\frac{\partial \mathcal{L}}{\partial s} = \frac{100}{2\sqrt{s}} - 500\lambda = 0$$

$$\frac{50}{\sqrt{s}} = 500\lambda \implies \lambda = \frac{1}{10\sqrt{s}}$$

$$\frac{\partial \mathcal{L}}{\partial \lambda} = -(500s - 150000) = 0 \implies s = 300$$

**Verification:**

From the budget constraint:
$$500s = 150000 \implies s = \frac{150000}{500} = \boxed{300 \text{ tons}}$$

---

**Note:** In this particular problem, since there's only **one variable (s)** and **one binding constraint (500s = 150,000)**, the constraint itself directly gives s = 300. The Lagrangian confirms this is indeed the **maximum** (not just a critical point), since R(s) = 100√s is a concave function — any feasible point is a global maximum on the constraint.

The answer is **300 tons** of raw steel to be purchased.
</details>


<img width="605" height="266" alt="image" src="https://github.com/user-attachments/assets/ea3808a8-4a27-4538-a27f-8a2a551f2f9b" />

<details>
  <summary>Sol</summary>

## Maximum Revenue Calculation

Using the optimal value found in Q10: **s = 300 tons**

**Substituting into the Revenue Function:**

$$R(s) = 100\sqrt{s}$$

$$R(300) = 100\sqrt{300}$$

$$= 100 \times \sqrt{300}$$

$$= 100 \times 17.3205...$$

$$\boxed{R(300) \approx 1732 \text{ Rs}}$$

---

**Quick breakdown of √300:**

$$\sqrt{300} = \sqrt{100 \times 3} = 10\sqrt{3} = 10 \times 1.7320... = 17.320...$$

So:
$$R(300) = 100 \times 17.320 = \textbf{1732 Rs}$$

The maximum revenue Krishna can earn within his budget of Rs. 1,50,000 is **Rs. 1732**.
  
</details>






<img width="869" height="697" alt="image" src="https://github.com/user-attachments/assets/24a2cefe-2ed5-42e5-9af3-26a207610479" />

<details>
  <summary>Sol</summary>

Good question! Here's exactly how:

## From Case B: g₁ and g₃ both active

$$0.5y_1 + y_2 = 6 \tag{i}$$
$$y_1 + 4y_2 = 13 \tag{ii}$$

---

## Step 1: Express y₁ in terms of y₂ (from equation i)

$$0.5y_1 = 6 - y_2$$
$$y_1 = 12 - 2y_2$$

---

## Step 2: Substitute into equation (ii)

$$(12 - 2y_2) + 4y_2 = 13$$
$$12 + 2y_2 = 13$$
$$2y_2 = 1$$
$$\boxed{y_2 = 0.5}$$

---

## Step 3: Substitute y₂ back into equation (i)

$$y_1 = 12 - 2(0.5)$$
$$y_1 = 12 - 1$$
$$\boxed{y_1 = 11}$$

---

Essentially it's just **solving two simultaneous equations** — treating the two active constraints as a simple 2×2 linear system.
  
</details>



</details>
