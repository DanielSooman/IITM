<details>
  <summary>Week9</summary>

<img width="923" height="429" alt="image" src="https://github.com/user-attachments/assets/c9fc62f0-0c7f-455c-bfec-3e31285bcdd5" />
<img width="1178" height="470" alt="image" src="https://github.com/user-attachments/assets/f1a5fd27-65ef-4492-a75b-2338a0f8651b" />
<img width="608" height="441" alt="image" src="https://github.com/user-attachments/assets/fe1f59a9-ceac-4646-8a89-586f23679fc0" />
<img width="739" height="444" alt="image" src="https://github.com/user-attachments/assets/accfa960-53d9-432e-9521-1971c5968fe9" />
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
