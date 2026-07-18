<img width="759" height="482" alt="image" src="https://github.com/user-attachments/assets/e46b66e9-983d-4901-ba02-f9b039873d4f" />
<img width="768" height="368" alt="image" src="https://github.com/user-attachments/assets/a0cb34c8-fe62-4e54-9ed2-871be7c65e17" />
<img width="1174" height="722" alt="image" src="https://github.com/user-attachments/assets/05442842-f344-4e1d-81e5-79fc1ee544df" />
<img width="1296" height="451" alt="image" src="https://github.com/user-attachments/assets/c5e6cbf9-c086-41ec-8632-6d83d9ab8fca" />
<img width="1269" height="645" alt="image" src="https://github.com/user-attachments/assets/4de2cce8-487b-4cba-8e27-75592b437b1b" />
<img width="1188" height="390" alt="image" src="https://github.com/user-attachments/assets/dabd89b7-729b-4e9f-ac87-21fa223f96a9" />
<img width="1188" height="390" alt="image" src="https://github.com/user-attachments/assets/769570b3-0a24-4a0c-a1fb-c749d8a7c941" />
<img width="1188" height="390" alt="image" src="https://github.com/user-attachments/assets/6cffdb8f-f2c3-4835-86bf-63682831da87" />
<img width="1411" height="502" alt="image" src="https://github.com/user-attachments/assets/3a0cb1d7-65f8-4ce1-87b8-ff4b695daed6" />
<img width="1411" height="502" alt="image" src="https://github.com/user-attachments/assets/552feccb-9216-4f8c-9c38-5f4d04417fb2" />
<img width="1330" height="419" alt="image" src="https://github.com/user-attachments/assets/539b47f6-bcf9-47ad-90e3-9d337dce4849" />
<img width="1383" height="462" alt="image" src="https://github.com/user-attachments/assets/6c51e849-9fc3-470a-960d-d30946240079" />
<img width="1425" height="638" alt="image" src="https://github.com/user-attachments/assets/91898087-8ca8-4568-b7de-70924eccf6e4" />
<img width="1213" height="490" alt="image" src="https://github.com/user-attachments/assets/36d57c55-da0e-4dce-96a4-7d086306fde3" />
<img width="1424" height="556" alt="image" src="https://github.com/user-attachments/assets/2fda10f5-1615-40d9-8be9-1a5a8745fce3" />




<details>
  <summary>PCA via centering</summary>

To compute the variance along the first principal component, we need to find the largest eigenvalue of the covariance matrix of the dataset $S$.

Depending on the convention used in your course (biased vs. unbiased covariance matrix), the calculation is as follows:

---

### Step 1: Compute the Mean of the Dataset

The dataset consists of $N = 4$ points:


$$S = \left\{ \begin{bmatrix} 0 \\ 0 \end{bmatrix}, \begin{bmatrix} 1 \\ 2 \end{bmatrix}, \begin{bmatrix} 3 \\ 6 \end{bmatrix}, \begin{bmatrix} 5 \\ 10 \end{bmatrix} \right\}$$

$$\mu_x = \frac{0 + 1 + 3 + 5}{4} = 2.25$$

$$\mu_y = \frac{0 + 2 + 6 + 10}{4} = 4.5$$

---

### Step 2: Center the Data

Subtract the mean from each point to get the centered data points ($x_i - \mu_x, y_i - \mu_y$):

* $\mathbf{x}_1' = \begin{bmatrix} 0 - 2.25 \\ 0 - 4.5 \end{bmatrix} = \begin{bmatrix} -2.25 \\ -4.5 \end{bmatrix}$
* $\mathbf{x}_2' = \begin{bmatrix} 1 - 2.25 \\ 2 - 4.5 \end{bmatrix} = \begin{bmatrix} -1.25 \\ -2.5 \end{bmatrix}$
* $\mathbf{x}_3' = \begin{bmatrix} 3 - 2.25 \\ 6 - 4.5 \end{bmatrix} = \begin{bmatrix} 0.75 \\ 1.5 \end{bmatrix}$
* $\mathbf{x}_4' = \begin{bmatrix} 5 - 2.25 \\ 10 - 4.5 \end{bmatrix} = \begin{bmatrix} 2.75 \\ 5.5 \end{bmatrix}$

---

### Step 3: Project onto the First Principal Component

Since all points are perfectly collinear along the line $y = 2x$, the first principal component points in the normalized direction of this line:


$$\mathbf{u} = \begin{bmatrix} \frac{1}{\sqrt{5}} \\ \frac{2}{\sqrt{5}} \end{bmatrix}$$

The projection distance of each centered point onto $\mathbf{u}$ is given by the dot product $\mathbf{x}_i'^T \mathbf{u}$:

* $d_1 = \frac{-2.25(1) + -4.5(2)}{\sqrt{5}} = \frac{-11.25}{\sqrt{5}}$
* $d_2 = \frac{-1.25(1) + -2.5(2)}{\sqrt{5}} = \frac{-6.25}{\sqrt{5}}$
* $d_3 = \frac{0.75(1) + 1.5(2)}{\sqrt{5}} = \frac{3.75}{\sqrt{5}}$
* $d_4 = \frac{2.75(1) + 5.5(2)}{\sqrt{5}} = \frac{13.75}{\sqrt{5}}$

---

### Step 4: Calculate Squared Distances (Total Sum of Squares)

The variance is computed using the sum of squared distances:


$$d_1^2 = \frac{126.5625}{5} = 25.3125$$

$$d_2^2 = \frac{39.0625}{5} = 7.8125$$

$$d_3^2 = \frac{14.0625}{5} = 2.8125$$

$$d_4^2 = \frac{189.0625}{5} = 37.8125$$

$$\text{Sum of Squares} = 25.3125 + 7.8125 + 2.8125 + 37.8125 = 73.75$$

---

### Final Answer (Choose based on your evaluation system)

> **Option A (Biased Covariance Matrix / Divided by $N=4$):**
> If your course defines standard PCA using $\frac{1}{N} \sum d_i^2$:
> 
> $$\text{Variance} = \frac{73.75}{4} = 18.4375 \rightarrow \mathbf{18.44}$$
> 
> 

> **Option B (Unbiased Covariance Matrix / Divided by $N-1=3$):**
> If your course follows standard software packages like `scikit-learn` that use sample variance $\frac{1}{N-1} \sum d_i^2$:
> 
> $$\text{Variance} = \frac{73.75}{3} = 24.5833... \rightarrow \mathbf{24.58}$$
> 
>
  
</details>
