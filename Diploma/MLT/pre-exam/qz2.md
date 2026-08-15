<details>
<summary>PYQs YT</summary>

- [T2-25](https://www.youtube.com/watch?v=mn5-A0NVvz8) 
- [T3-23](https://www.youtube.com/watch?v=fKHIbr7c7hQ)
- 
</details>






Based on the revision sessions for Weeks 5 to 8, here are the essential formulas and mathematical concepts you need to know for Quiz 2:

### **1. Linear Regression and Regularization (Weeks 5 & 6)**

*   **Linear Model:** The basic model for regression is \\(y = w^T x\\), where \\(w\\) is the **weight vector** and \\(x\\) represents the features.
*   **Closed-Form Solution (Normal Equation):** The optimal weights (\\(w^*\\)) that minimize the sum of squared errors are calculated as:
    \\[w^* = (XX^T)^{-1}XY\\]
    Note: This is often referred to as the **Maximum Likelihood Estimate (MLE)** under the assumption of Gaussian noise.
*   **Gradient Descent Update Rule:** To find weights iteratively, use:
    \\[w_{t+1} = w_t - \eta \nabla f(w_t)\\]
    where \\(\eta\\) is the **learning rate** and \\(\nabla f(w_t)\\) is the gradient of the loss function.
*   **Mean Squared Error (MSE) vs. Mean Absolute Error (MAE):**
    *   **MSE:** \\(\frac{1}{n} \sum_{i=1}^{n} (w^T x_i - y_i)^2\\). This is used when assuming **Gaussian noise**.
    *   **MAE:** \\(\frac{1}{n} \sum_{i=1}^{n} |w^T x_i - y_i|\\). This is used when assuming **Laplace noise** and is more **robust to outliers**.
*   **Regularization (Ridge and Lasso):**
    *   **Ridge (\\(L2\\)):** Minimizes \\(MSE + \lambda ||w||_2^2\\). The closed-form solution is \\(w_{ridge} = (XX^T + \lambda I)^{-1}XY\\).
    *   **Lasso (\\(L1\\)):** Minimizes \\(MSE + \lambda ||w||_1\\). It encourages **sparsity** (setting some weights exactly to zero).
*   **Kernel Regression:**
    *   **Dual Weights:** \\(\alpha^* = K^{-1}y\\), where \\(K\\) is the kernel matrix (\\(X^T X\\)).
    *   **Prediction:** \\(\hat{y} = \sum_{i=1}^{n} \alpha_i^* K(x_i, x_{test})\\).

### **2. Classification and Decision Trees (Week 7)**

*   **0-1 Loss (Misclassification Rate):** The average number of incorrect predictions:
    \\[\text{Loss} = \frac{1}{n} \sum_{i=1}^{n} I(\hat{y}_i \neq y_i)\\]
    where \\(I\\) is an indicator function that equals 1 if the condition is true.
*   **Entropy (\\(H\\)):** Measures the **impurity** of a node:
    \\[H(p) = -p \log_2(p) - (1-p) \log_2(1-p)\\]
    Important values to remember: \\(H(0) = 0\\), \\(H(1) = 0\\), and \\(H(0.5) = 1\\).
*   **Weighted Entropy of Children:** To evaluate a split, calculate the weighted average of the children's entropy:
    \\[H_{children} = \frac{n_{left}}{n} H(p_{left}) + \frac{n_{right}}{n} H(p_{right})\\].
*   **Information Gain (IG):** The reduction in entropy after a split:
    \\[IG = H(Parent) - H_{children}\\].

### **3. Generative Models and Naive Bayes (Week 8)**

*   **Number of Parameters (\\(D\\) features, \\(C\\) classes, each feature taking \\(K\\) values):**
    *   **Full Generative Model:** \\(C(K^D - 1) + (C - 1)\\).
    *   **Naive Bayes Model:** \\(CD(K - 1) + (C - 1)\\). For binary features (\\(K=2\\)) and two classes (\\(C=2\\)), this simplifies to **\\(2D + 1\\)**.
*   **Naive Bayes Prediction:** The predicted class is the one that maximizes the joint probability:
    \\[P(Y=c|X) \propto P(Y=c) \prod_{j=1}^{D} P(X_j | Y=c)\\].
*   **Maximum Likelihood Estimates (MLE):**
    *   **Prior:** \\(\hat{P}(Y=c) = \frac{N_c}{N}\\) (number of points in class \\(c\\) divided by total points).
    *   **Class Conditional:** \\(\hat{P}(X_j=1 | Y=c) = \frac{\text{count}(X_j=1 \text{ in class } c)}{N_c}\\).
*   **Laplace Smoothing:** To avoid zero probabilities, add dummy data points. The general formula for binary features is:
    \\[\hat{P}_{smoothed} = \frac{\text{count} + 1}{N_c + 2}\\]
    This effectively adds one "all ones" and one "all zeros" data point to each class.
