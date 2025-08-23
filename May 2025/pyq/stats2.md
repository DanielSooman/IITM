
<img width="1020" height="611" alt="image" src="https://github.com/user-attachments/assets/e83c23d7-d6d9-4edc-8320-9e4d6f8449ee" />


The correct moment generating function (MGF) for the random variable $S = X_1 + X_2 + X_3$ is the third option:
$$M_S(\lambda) = \left(\frac{e^{-0.2\lambda} + e^{0.2\lambda}}{2}\right)^3$$
---
## How to Find the MGF

### Step 1: Understand the Moment Generating Function
The moment generating function, or MGF, of a random variable **X** is defined as $M_X(\lambda) = E[e^{\lambda X}]$. It's a useful tool in probability theory because it uniquely determines the probability distribution of a random variable and can simplify calculations involving sums of independent random variables.

### Step 2: Find the MGF of a Single Uniform Random Variable
The random variable **X** is uniformly distributed on the set $\{-0.2, 0.2\}$. This means that X can take on two values, $-0.2$ and $0.2$, each with a probability of $1/2$.
So, the MGF of a single random variable **X** is:
$$M_X(\lambda) = E[e^{\lambda X}] = \sum_{x \in \{-0.2, 0.2\}} e^{\lambda x} P(X=x)$$
$$M_X(\lambda) = e^{\lambda(-0.2)} \cdot P(X=-0.2) + e^{\lambda(0.2)} \cdot P(X=0.2)$$
Since the probabilities are equal, $P(X=-0.2) = P(X=0.2) = 1/2$.
$$M_X(\lambda) = e^{-0.2\lambda} \cdot \frac{1}{2} + e^{0.2\lambda} \cdot \frac{1}{2} = \frac{e^{-0.2\lambda} + e^{0.2\lambda}}{2}$$

### Step 3: Find the MGF for the Sum of Independent and Identically Distributed Random Variables
The problem states that $X_1, X_2,$ and $X_3$ are independent and identically distributed (i.i.d.). This is a crucial piece of information because it simplifies finding the MGF of their sum. For i.i.d. random variables, the MGF of their sum is the product of their individual MGFs.
$$M_S(\lambda) = M_{X_1+X_2+X_3}(\lambda) = M_{X_1}(\lambda) \cdot M_{X_2}(\lambda) \cdot M_{X_3}(\lambda)$$
Since they are identically distributed, their MGFs are all the same: $M_{X_1}(\lambda) = M_{X_2}(\lambda) = M_{X_3}(\lambda) = M_X(\lambda)$.
$$M_S(\lambda) = \left(M_X(\lambda)\right)^3$$
Substituting the expression for $M_X(\lambda)$ we found in the previous step:
$$M_S(\lambda) = \left(\frac{e^{-0.2\lambda} + e^{0.2\lambda}}{2}\right)^3$$
This matches the third option provided in the problem.






<img width="1008" height="673" alt="image" src="https://github.com/user-attachments/assets/a1eb1b6e-cb09-4d2b-8511-06fabbd871c0" />


The level of significance is given by the probability of rejecting the null hypothesis when it's true. For the given problem, this is the probability that $T < c$ under the null hypothesis $H_0: \mu = 4$.

---

### Step-by-Step Solution

Under the null hypothesis $H_0: \mu = 4$, the sample mean $\bar{X} = \frac{1}{100}\sum_{i=1}^{100} X_i$ is normally distributed with a mean of $\mu_0 = 4$ and a variance of $\sigma^2/n = 36/100 = 0.36$. So, $\bar{X} \sim \text{Normal}(4, 0.36)$.

The test statistic is defined as $T = \frac{X_1 + X_2 + \ldots + X_{100}}{100} = \bar{X}$. The test rejects $H_0$ if $T < c$. The level of significance, denoted by $\alpha$, is the probability of this event occurring when $H_0$ is true.

$\alpha = P(T < c | H_0 \text{ is true}) = P(\bar{X} < c | \mu = 4)$.

To find this probability, we standardize the random variable $\bar{X}$ to a standard normal variable $Z$. The formula for standardization is $Z = \frac{\bar{X} - \mu_{\bar{X}}}{\sigma_{\bar{X}}}$, where $\mu_{\bar{X}} = 4$ and $\sigma_{\bar{X}} = \sqrt{0.36} = 0.6$.

$Z = \frac{\bar{X} - 4}{0.6}$.

Now, we can express the probability in terms of $Z$:

$\alpha = P\left(\frac{\bar{X} - 4}{0.6} < \frac{c - 4}{0.6}\right) = P\left(Z < \frac{c - 4}{0.6}\right)$.

Let $F_Z(z)$ be the cumulative distribution function (CDF) of the standard normal variable $Z$. Then, $P(Z < z) = F_Z(z)$.

Therefore, $\alpha = F_Z\left(\frac{c - 4}{0.6}\right)$.

To match the options provided, we need to simplify the expression inside the parentheses:

$\frac{c - 4}{0.6} = \frac{c - 4}{6/10} = \frac{10(c - 4)}{6} = \frac{5(c - 4)}{3} = \frac{5c - 20}{3}$.

So, the level of significance is $\alpha = F_Z\left(\frac{5c - 20}{3}\right)$.

This corresponds to the **fourth option** in the provided image.


