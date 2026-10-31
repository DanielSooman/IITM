
## Stage 1 — Transcription

All text is readable; no answer-changing parts are unclear. Each question is worth **1 mark**. No negative marking is shown.

### Q1 — Multi-select
**Which of the following functions have saddle points at \((0,0)\)?**

- **A.** \(x^2+y^2\)
- **B.** \(x^3-3xy^2\)
- **C.** \(x^4+y^4-4xy\)
- **D.** \(x^4+y^4\)

### Q2 — Multi-select
While using vanilla gradient descent to minimize
\[
f(w_1,w_2)=0.1w_1^3+10w_2^3,
\]
what type of learning rate is preferred for variables \(w_1\) and \(w_2\)?

- **A.** Learning rate should be same for both \(w_1\) and \(w_2\).
- **B.** For \(w_1\), a small learning rate as the gradients in the direction of \(w_1\) are small.
- **C.** For \(w_1\), a high learning rate as the gradients in the direction of \(w_1\) are small.
- **D.** For \(w_2\), a small learning rate as the gradients in the direction of \(w_2\) are high.
- **E.** For \(w_2\), a high learning rate as the gradients in the direction of \(w_2\) are high.

### Q3 — Numeric
\[
f(x,y)=x^2+y^2
\]
Learning rate \(\eta=0.1\). Momentum is
\[
v_t=\beta v_{t-1}+\nabla f_t,\qquad
(x_{t+1},y_{t+1})=(x_t,y_t)-\eta v_t,
\]
where \(v_{-1}=0\).

Starting from the same non-origin point, the result after **three vanilla-GD updates** equals the result after **two momentum-GD updates**. Find \(\beta\).

### Q4 — Single-select
Losses, with \(x_0=2.0\):

1. \(L_1=x\)
2. \(L_2=x^2\)
3. \(L_3=x^3\)
4. \(L_4=\log(x)\)

Using momentum gradient descent with \(\beta=0.9\), learning rate \(0.1\), and 10 iterations, which loss has faster parameter updates (larger changes in \(x\)) during the initial iterations?

- **A.** \(L_1=x\)
- **B.** \(L_2=x^2\)
- **C.** \(L_3=x^3\)
- **D.** \(L_4=\log(x)\)

### Q5 — Single-select
Feature A appears in almost every sample; feature B appears in only 2% of samples. Both have the same initial gradient magnitude. After 100 iterations, A’s weight almost stops changing while B’s weight still slowly increases. Which optimizer is most likely used?

- **A.** Gradient Descent
- **B.** Momentum-based Gradient Descent
- **C.** Nesterov Optimizer
- **D.** Adagrad

### Q6 — Single-select
In PyTorch, which argument controls whether SGD behaves as Batch, Mini-Batch, or Stochastic Gradient Descent?

- **A.** Optimizer type (`torch.optim.SGD`)
- **B.** Loss function
- **C.** `batch_size` in `DataLoader`
- **D.** Number of epochs

### Q7 — Single-select
For a dataset of \(N\) samples and `num_epochs = 10`, which correctly gives the total number of optimizer-update steps?

- **A.** BGD: `num_epochs * N`; SGD: `num_epochs * 1`
- **B.** BGD: `num_epochs`; SGD: `num_epochs`
- **C.** BGD: `N`; SGD: `num_epochs * N * P`
- **D.** BGD: `num_epochs * 1`; SGD: `num_epochs * N`

### Q8 — Single-select
For mini-batch gradient descent:

```python
for ep in range(epochs):
    indices = np.random.permutation(n)
    X_shuffled = X[indices]
    y_shuffled = y[indices]

    for batch_idx in range(n_batch):
        start_idx = batch_idx*batch_size
        ____________________________  # placeholder

        X_batch = X_shuffled[start_idx:end_idx]
        y_batch = y_shuffled[start_idx:end_idx]
```

- **A.** `end_idx = int(min(start_idx + batch_size, n))`
- **B.** `end_idx = int(min(batch_size, n))`
- **C.** `end_idx = batch_size`
- **D.** `end_idx = int(min(start_idx + batch_size, batch_size + n))`

### Q9 — Single-select
Complete the missing Adam bias-correction parts:

- **A.** `m/beta1` and `v/beta2`
- **B.** `m/(1-beta1)` and `v/(1-beta2)`
- **C.** `m/np.sqrt(np.square(m).sum())` and `v/np.sqrt(np.square(v).sum())`
- **D.** `m/(1-beta1**t)` and `v/(1-beta2**t)`

---

# Answers and checks

### Q1: **B and C**

- **A excluded:** \(x^2+y^2\ge0\), so \((0,0)\) is a local/global minimum, not a saddle.
- **B included:** Along \(y=0\), \(f(x,0)=x^3\), which is positive for \(x>0\) and negative for \(x<0\). Thus values on both sides of \(0\) occur arbitrarily near the point.
- **C included:** Along \(y=0\), \(f(x,0)=x^4>0\). Along \(y=x=t\),
  \[
  f(t,t)=2t^4-4t^2<0
  \]
  for sufficiently small nonzero \(t\). Both signs occur, so it is a saddle.
- **D excluded:** \(x^4+y^4\ge0\), hence \((0,0)\) is a minimum.

---

### Q2: **C and D**

\[
\frac{\partial f}{\partial w_1}=0.3w_1^2,\qquad
\frac{\partial f}{\partial w_2}=30w_2^2.
\]

For comparable values of \(w_1,w_2\), the gradient scale in the \(w_2\) direction is much larger than in the \(w_1\) direction.

- **A excluded:** Equal learning rates do not account for the strongly different gradient scales.
- **B excluded:** A small gradient direction typically needs a relatively **larger** learning rate.
- **C included:** \(w_1\) has the smaller gradient scale, so it can use a higher learning rate.
- **D included:** \(w_2\) has the larger gradient scale, so it should use a smaller learning rate.
- **E excluded:** A high learning rate combined with large gradients risks overshooting/divergence.

---

### Q3: **0.64**

Let \(p_t\) denote either coordinate, since \(x\) and \(y\) follow the same update rule.

For vanilla GD:
\[
p_{t+1}=p_t-0.1(2p_t)=0.8p_t.
\]
After three updates:
\[
p_3=(0.8)^3p_0=0.512p_0.
\]

For momentum GD:

\[
v_0=2p_0,\qquad p_1=p_0-0.1v_0=0.8p_0.
\]

Then:
\[
v_1=\beta v_0+2p_1
=2\beta p_0+1.6p_0.
\]

So:
\[
p_2=p_1-0.1v_1
=0.8p_0-0.1(2\beta+1.6)p_0
=(0.64-0.2\beta)p_0.
\]

Set this equal to the vanilla-GD result after three updates:
\[
0.64-0.2\beta=0.512.
\]
\[
0.2\beta=0.128,\qquad \beta=0.64.
\]

**Final answer: `0.64`**

---

### Q4: **C — \(L_3=x^3\)**

At \(x_0=2\), the gradients are:

\[
L_1'=1,\qquad
L_2'=2x=4,\qquad
L_3'=3x^2=12,\qquad
L_4'=\frac1x=0.5.
\]

With initial momentum zero, the first update magnitudes are proportional to these gradients:

\[
0.1,\quad 0.4,\quad 1.2,\quad 0.05.
\]

Thus \(x^3\) produces the largest initial update, and its momentum remains large in the next few steps.

- **A excluded:** gradient magnitude is only \(1\).
- **B excluded:** initial gradient is \(4\), below \(12\).
- **C included:** initial gradient is \(12\), the largest.
- **D excluded:** initial gradient is \(0.5\), the smallest.

---

### Q5: **D — Adagrad**

Adagrad uses a separate accumulated squared-gradient term for each parameter:

\[
\text{effective learning rate}_i
\propto \frac{1}{\sqrt{\sum_t g_{i,t}^2}}.
\]

Feature A appears frequently, so its accumulated gradient square becomes large and its effective learning rate shrinks substantially. Feature B is sparse, so its accumulator grows slowly and it continues changing.

- **A/B/C excluded:** They do not specifically reduce learning rates based on per-feature gradient frequency in this way.
- **D included:** This is the characteristic Adagrad behavior for frequent versus sparse features.

---

### Q6: **C — `batch_size` in `DataLoader`**

- **A excluded:** `torch.optim.SGD` specifies the optimization rule, not how many samples are used per update.
- **B excluded:** The loss function does not choose batch versus stochastic behavior.
- **C included:** `batch_size=1` gives SGD; `batch_size=N` gives batch GD; intermediate values give mini-batch GD.
- **D excluded:** Epoch count changes training duration, not samples per update.

---

### Q7: **D**

- Batch GD performs **one** update after processing all \(N\) samples in each epoch:
  \[
  \text{total updates} = \text{num\_epochs}\times1.
  \]
- SGD performs **one update per sample**, hence \(N\) updates per epoch:
  \[
  \text{total updates} = \text{num\_epochs}\times N.
  \]

- **A excluded:** Reverses BGD and SGD counts.
- **B excluded:** Incorrectly gives SGD only one update per epoch.
- **C excluded:** Omits epochs for BGD and incorrectly includes \(P\); each optimizer step updates the entire parameter vector.
- **D included:** Correct.

---

### Q8: **A**

```python
end_idx = int(min(start_idx + batch_size, n))
```

This advances the end index by one batch while ensuring the final incomplete batch stops at dataset length \(n\).

- **B excluded:** Does not account for `start_idx`.
- **C excluded:** Same issue; later batches would have invalid/empty slices.
- **D excluded:** Uses `batch_size + n` rather than the valid dataset boundary \(n\).

---

### Q9: **D**

Adam’s bias corrections are:

\[
\hat m_t=\frac{m_t}{1-\beta_1^t},
\qquad
\hat v_t=\frac{v_t}{1-\beta_2^t}.
\]

- **A excluded:** Dividing by \(\beta_1,\beta_2\) is not bias correction.
- **B excluded:** Only matches the first iteration (\(t=1\)); it omits the exponent \(t\).
- **C excluded:** This is a norm-like normalization, not Adam bias correction.
- **D included:** Correct formula.

---

## Final answer key

| Question | Answer |
|---|---|
| 1 | **B, C** |
| 2 | **C, D** |
| 3 | **0.64** |
| 4 | **C** |
| 5 | **D** |
| 6 | **C** |
| 7 | **D** |
| 8 | **A** |
| 9 | **D** |

## Verification summary

I used separate direct-derivation, option-elimination, and substitution/index-check passes. In particular, I checked Q1 by directional sign tests, Q3 by substituting \(\beta=0.64\) back into the recurrence, Q7 by counting updates per epoch, Q8 with final-batch indexing, and Q9 against the Adam definition. No code-execution or independent subagent tool was available in this chat.

**Confidence: Medium overall.** Q1 and Q3–Q9 are high-confidence from direct mathematical/algorithmic checks. Q2’s intended answer is clearly **C and D**, but strictly its relative gradient magnitudes depend on the current values of \(w_1,w_2\); it assumes comparable coordinate scales, as such introductory optimizer questions normally do.
