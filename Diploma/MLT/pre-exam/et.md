<img width="1126" height="258" alt="image" src="https://github.com/user-attachments/assets/d968bbc8-99b8-4c8d-8b4a-2b0353b23f73" />
<img width="939" height="330" alt="image" src="https://github.com/user-attachments/assets/e3a502d8-6387-48c3-8ae7-01164f5a68df" />
<img width="993" height="401" alt="image" src="https://github.com/user-attachments/assets/e28ad296-298a-43e0-99d5-aa1f5cfdd53f" />
<img width="983" height="587" alt="image" src="https://github.com/user-attachments/assets/02ecd494-5481-4230-a178-bb2b0aada087" />


<details>
  <summary>Entropy</summary>

  **Information Gain** measures how much cleaner or less mixed a group becomes after splitting it.

$$\text{Information Gain} = \text{Parent Entropy} - \text{Weighted Child Entropy}$$

---

### Step 1: Calculate Parent Entropy (Initial Mix)

The dataset has 8 total points with labels $y$:

* 5 points have label $+1$
* 3 points have label $-1$

$$\text{Entropy}(P) = -\left(\frac{5}{8}\log_2 \frac{5}{8} + \frac{3}{8}\log_2 \frac{3}{8}\right) \approx 0.9544$$

---

### Step 2: Calculate Child Entropies (After Split $x < 0$)

* **Left Branch ($x < 0$):** 4 points $\{(-4,1), (-3,1), (-2,1), (-1,1)\}$
* All 4 points have label $+1$ (perfectly pure group).
* $\text{Entropy}(\text{Left}) = 0$


* **Right Branch ($x \ge 0$):** 4 points $\{(1,-1), (2,-1), (3,-1), (4,1)\}$
* 1 point has label $+1$, 3 points have label $-1$.
* $\text{Entropy}(\text{Right}) = -\left(\frac{1}{4}\log_2 \frac{1}{4} + \frac{3}{4}\log_2 \frac{3}{4}\right) \approx 0.8113$



---

### Step 3: Calculate Weighted Average of Children

Each child gets half of the 8 total points ($\frac{4}{8}$ each):

$$\text{Weighted Entropy} = \frac{4}{8}(0) + \frac{4}{8}(0.8113) = 0.4056$$

---

### Step 4: Calculate Information Gain

$$\text{Information Gain} = 0.9544 - 0.4056 = 0.5488$$

---

**Final Answer:** **`0.549`**
  
</details>
