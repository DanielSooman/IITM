<details>
<summary>PYQs YT</summary>

- [T2-25](https://www.youtube.com/watch?v=mn5-A0NVvz8) 
- [T3-23](https://www.youtube.com/watch?v=fKHIbr7c7hQ)
- 
</details>



# Quiz 2 — Weeks 5–8 Essential Formulas

## 1. Linear Regression and Regularization — Weeks 5 & 6

### Linear Model

The basic regression model is:

$$
y = w^T x
$$

where:
- $w$ = weight vector
- $x$ = feature vector

### Closed-Form Solution — Normal Equation

The optimal weights are:

$$
w^* = (XX^T)^{-1}XY
$$

This is also the **Maximum Likelihood Estimate (MLE)** under the assumption of **Gaussian noise**.

### Gradient Descent

The weight update rule is:

$$
w_{t+1} = w_t - \eta \nabla f(w_t)
$$

where:
- $\eta$ = learning rate
- $\nabla f(w_t)$ = gradient of the loss function

### Mean Squared Error — MSE

$$
MSE = \frac{1}{n}\sum_{i=1}^{n}(w^T x_i-y_i)^2
$$

- Used when assuming **Gaussian noise**.
- Squaring makes large errors more important.

### Mean Absolute Error — MAE

$$
MAE = \frac{1}{n}\sum_{i=1}^{n}|w^T x_i-y_i|
$$

- Used when assuming **Laplace noise**.
- More **robust to outliers** than MSE.


### Regularization

Regularization helps prevent overfitting by penalizing large weights.

#### Ridge Regression — $L2$

Objective:

$$
MSE+\lambda\|w\|_2^2
$$

Closed-form solution:

$$
w_{\text{ridge}}=
(XX^T+\lambda I)^{-1}XY
$$

#### Lasso Regression — $L1$

Objective:

$$
MSE+\lambda\|w\|_1
$$

Key property:

- Encourages **sparsity**.
- Can make some weights **exactly zero**.


### Kernel Regression

#### Dual Weights

$$
\alpha^*=K^{-1}y
$$

where $K$ is the kernel matrix.

#### Prediction


$$
\hat{y}=
\sum_{i=1}^{n}
\alpha_i^*K(x_i,x_{\text{test}})
$$


# 2. Classification and Decision Trees — Week 7

## 0–1 Loss

Measures the fraction of incorrect predictions:

$$
\text{Loss}=
\frac{1}{n}
\sum_{i=1}^{n}
I(\hat{y}_i\neq y_i)
$$

where $I$ is the **indicator function**:

- $I(\text{true})=1$
- $I(\text{false})=0$


## Entropy

Entropy measures the **impurity** of a node.

$$
H(p) =
-p\log_2(p)
-(1-p)\log_2(1-p)
$$

### Important Values

$$
H(0)=0
$$

$$
H(1)=0
$$

$$
H(0.5)=1
$$

### Remember

- Pure node → **Entropy = 0**
- Maximum uncertainty → **Entropy = 1** for binary classification


## Weighted Entropy of Children

For a binary split:

$$
H_{\text{children}} =
\frac{n_{\text{left}}}{n}H(p_{\text{left}})
+
\frac{n_{\text{right}}}{n}H(p_{\text{right}})
$$


## Information Gain

Information Gain measures the reduction in entropy after a split:

$$
IG=
H(\text{Parent})-
H(\text{Children})
$$

Higher Information Gain → **better split**.


# 3. Generative Models and Naive Bayes — Week 8

## Number of Parameters

Suppose:

- $D$ = number of features
- $C$ = number of classes
- $K$ = number of possible values for each feature

### Full Generative Model

$$
C(K^D-1)+(C-1)
$$

### Naive Bayes Model

$$
CD(K-1)+(C-1)
$$

### Binary Features and Two Classes

For:

$$
K=2,\qquad C=2
$$

the number of parameters becomes:

$$
2D+1
$$


## Naive Bayes Prediction

Choose the class that maximizes:

$$
P(Y=c\mid X)
\propto
P(Y=c)
\prod_{j=1}^{D}
P(X_j\mid Y=c)
$$

In simple terms:

$$
\boxed{
\text{Prior}\times\text{Likelihood}
}
$$

Choose the class with the **largest probability**.


## Maximum Likelihood Estimates — MLE

### Prior Probability

$$
\hat{P}(Y=c)=
\frac{N_c}{N}
$$

where:
- $N_c$ = number of observations in class $c$
- $N$ = total number of observations

### Class-Conditional Probability

For a binary feature:

$$
\hat{P}(X_j=1\mid Y=c)=
\frac{
\text{count}(X_j=1\text{ in class }c)
}{
N_c
}
$$


## Laplace Smoothing

Used to avoid **zero probabilities**.

For binary features:

$$
\hat{P}_{\text{smoothed}}=
\frac{\text{count}+1}{N_c+2}
$$

This effectively adds:

- One **1**
- One **0**

to each class.


# Quick Formula Revision

| Topic | Formula |
|---|---|
| Linear Regression | $y=w^Tx$ |
| Normal Equation | $w^*=(XX^T)^{-1}XY$ |
| Gradient Descent | $w_{t+1}=w_t-\eta\nabla f(w_t)$ |
| MSE | $\frac{1}{n}\sum(w^Tx_i-y_i)^2$ |
| MAE | $\frac{1}{n}\sum(w^Tx_i-y_i)$ |
| Ridge | $MSE+\lambda\|w\|_2^2$ |
| Ridge Solution | $(XX^T+\lambda I)^{-1}XY$ |
| Lasso | $MSE+\lambda\|w\|_1$ |
| Kernel Weights | $\alpha^*=K^{-1}y$ |
| 0–1 Loss | $\frac{1}{n}\sum I(\hat y_i\neq y_i)$ |
| Entropy | $-p\log_2p-(1-p)\log_2(1-p)$ |
| Information Gain | $H(Parent)-H(Children)$ |
| Full Generative Parameters | $C(K^D-1)+(C-1)$ |
| NB Parameters | $CD(K-1)+(C-1)$ |
| Binary NB, $C=2$ | $2D+1$ |
| NB Prediction | $P(Y=c)\prod_jP(X_j\mid Y=c)$ |
| Prior MLE | $N_c/N$ |
| Conditional MLE | $\text{count}/N_c$ |
| Laplace Smoothing | $(\text{count}+1)/(N_c+2)$ |

## Highest-Priority Concepts

1. Calculate **MSE and MAE**.
2. Apply a **gradient descent update**.
3. Calculate **Ridge weights**.
4. Calculate **entropy**.
5. Calculate **weighted entropy**.
6. Calculate **Information Gain**.
7. Count parameters in **generative vs. Naive Bayes models**.
8. Calculate **Naive Bayes probabilities**.
9. Apply **Laplace smoothing**.
10. Remember:
   - **Gaussian noise → MSE**
   - **Laplace noise → MAE**
   - **Lasso → sparsity**
   - **Higher Information Gain → better split**
   - **Laplace smoothing → avoids zero probabilities**





---


<details>
<summary>Theory</summary>

<img width="1001" height="290" alt="image" src="https://github.com/user-attachments/assets/b814c4e4-cfb2-43b4-a0f8-4c957821eb26" />

</details>
