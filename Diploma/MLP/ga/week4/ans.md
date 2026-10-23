# Capability check
- I can read the 10 screenshots in the PDF (page 11 is just an advertisement, ignored).
- No subagents and no code execution are available in this session, so Stages 2–4 were run as separate passes in one context (weaker than true independent solvers – reflected in the confidence levels). All questions are conceptual/API-knowledge (scikit-learn), so "mechanical verification" here means checking each option against the documented scikit-learn behaviour, not running code.

# Stage 1 – Transcription (please skim for misreads)

| # | Type | Stem | Options |
|---|---|---|---|
| 1 | MCQ | Effect of increasing regularization parameter alpha in Ridge Regression? | a. increases model complexity · b. reduces model complexity · c. no effect · d. increases sensitivity to training data |
| 2 | MCQ (**incorrect**) | Which statement about Naïve Bayes is **incorrect**? | a. assumes conditional independence of features given class · b. GaussianNB suits continuous features · c. MultinomialNB commonly used for text · d. NB **always** outperforms logistic regression on **all** datasets |
| 3 | MCQ | Purpose of `hidden_layer_sizes` in MLPClassifier? | a. number of layers in the MLP · b. activation of output layer · c. number of neurons in each hidden layer · d. controls learning rate |
| 4 | MCQ | VotingClassifier with weights=[1,2,3] for three classifiers – effect? | a. number of features per estimator · b. influence of each estimator on prediction · c. order estimators are considered · d. weights for classes |
| 5 | MSQ | Which algorithms **may be** impacted by feature scaling? | a. Linear Regression · b. Decision Tree · c. SVM · d. NaiveBayes |
| 6 | MSQ | Which are true? | a. KNN low n_neighbors → complex boundaries · b. KNN low n_neighbors → smooth boundaries · c. feature scale impacts KNN boundaries · d. None of the above |
| 7 | MSQ | Techniques used in decision trees to make decisions / measure split quality during training? | a. Random Sampling · b. RoC Curve · c. Information Gain · d. Gini Impurity |
| 8 | MSQ | True regarding RandomForestClassifier? | a. randomness from bootstrap="true" or max_features < n_features · b. oob_score gives generalization score when bootstrap="true" · c. class_weight associates weights with classes · d. when bootstrap="False", max_samples decides number of samples drawn per base estimator |
| 9 | MSQ | Techniques for hyperparameter tuning in Ridge Regression? | a. GridSearchCV · b. ElasticNetCV · c. RandomizedSearchCV · d. Mini batch gradient descent |
| 10 | MSQ | True regarding logistic regression? | a. powerful for regression tasks (income, house price, sales) · b. predict_proba(X) gives per-class probabilities · c. penalty parameter decides type of regularization · d. max_iter=100 ensures **exactly** 100 iterations |

Nothing unclear in the text. Each question is 1 mark; no negative-marking info shown.

# Stage 2–5 – Solutions, elimination, and review

**Q1 → B (reduces complexity)**
Ridge minimises ‖y−Xw‖² + α‖w‖². Larger α shrinks the coefficients toward zero → simpler, higher-bias / lower-variance model.
- A ✗ opposite direction. C ✗ α directly changes the objective. D ✗ larger α makes the fit *less* sensitive to training data (that's the whole point of regularization).
- Check by limiting case: α→∞ gives w→0 (constant model, minimal complexity). ✔

**Q2 → D** (the *incorrect* statement; re-read the "incorrect" wording)
- A ✓ true – this is the "naïve" assumption. B ✓ true – GaussianNB models each continuous feature with a normal distribution. C ✓ true – MultinomialNB on word counts/TF-IDF is the classic text baseline.
- D ✗ false – "always … all datasets" contradicts the no-free-lunch principle; logistic regression often wins with enough data. So D is the incorrect statement → answer D.

**Q3 → C**
scikit-learn doc: `hidden_layer_sizes`: "The ith element represents the number of neurons in the ith hidden layer."
- A ✗ the tuple's *length* implies the number of *hidden* layers, but it does not set "the number of layers in the MLP" (input/output layers are fixed by data); the documented purpose is neuron counts. B ✗ output activation is chosen automatically (logistic/softmax). D ✗ that's `learning_rate_init` / `learning_rate`.

**Q4 → B**
`weights` in VotingClassifier: "Sequence of weights to weight the occurrences of predicted class labels (hard voting) or class probabilities before averaging (soft voting)." → the third classifier counts 3× as much as the first.
- A ✗ that's `max_features` in ensembles like RandomForest. C ✗ no notion of order in voting. D ✗ class weights are set per-estimator via `class_weight`, not here.

**Q5 → A and C (Linear Regression, SVM)**
- C ✓ SVM: margin/kernel are distance-based; unscaled features dominate the margin → strongly affected.
- A ✓ Linear Regression "may be" impacted: gradient-descent solvers (SGDRegressor) converge badly on unscaled data, and any regularized variant (Ridge/Lasso) penalises coefficients whose magnitude depends on feature scale. (Pure closed-form OLS *predictions* are scale-invariant, which is why the stem says "may be".)
- B ✗ Decision trees split on thresholds of one feature at a time; monotonic rescaling leaves the splits (and the tree) identical.
- D ✗ Naive Bayes fits each feature's distribution per class independently; rescaling a feature changes every class's likelihood by the same factor, so posteriors are unchanged. Standard course lists put NB and trees in the "not affected" group.

**Q6 → A and C**
- A ✓ k=1 memorises every point → highly irregular (complex) boundary; larger k smooths it.
- B ✗ the reverse of A. C ✓ KNN uses Euclidean distance, so a feature with large range dominates the neighbour choice. D ✗ since A and C are true.

**Q7 → C and D**
- C ✓ Information gain (entropy reduction) and D ✓ Gini impurity are the split criteria (`criterion='gini' | 'entropy' | 'log_loss'` in DecisionTreeClassifier).
- A ✗ random sampling (bootstrap) belongs to Random Forest/bagging, not to a single tree's split decision. B ✗ ROC curve is a post-hoc evaluation metric, not used while growing the tree.

**Q8 → A, B and C**
- A ✓ the two randomness sources in RF are bootstrap sampling of rows and random feature subsets at each split (`max_features`).
- B ✓ `oob_score` – "Only available if bootstrap=True"; it gives an estimate of generalization accuracy.
- C ✓ `class_weight` accepts a dict / 'balanced' / 'balanced_subsample'.
- D ✗ `max_samples` doc: "If bootstrap is True, the number of samples to draw from X to train each base estimator." With bootstrap=False the whole dataset is used for every tree and max_samples is ignored (an error is raised in recent versions if you set it). The statement inverts the condition → false.

**Q9 → A and C**
- A ✓ GridSearchCV and C ✓ RandomizedSearchCV search over `alpha` (and `solver`, etc.) for `Ridge`. (RidgeCV would also work but is not listed.)
- B ✗ ElasticNetCV tunes `alpha`/`l1_ratio` *for an ElasticNet model*; it is not a tuner for a Ridge estimator (and l1_ratio≈0 is documented as unreliable in coordinate descent).
- D ✗ mini-batch gradient descent is an optimisation algorithm for fitting the *weights*, not a hyperparameter-search technique.

**Q10 → B and C**
- A ✗ despite its name, logistic regression is a classifier; income/house price/sales are regression targets.
- B ✓ `predict_proba` returns an (n_samples, n_classes) array of class probabilities.
- C ✓ `penalty ∈ {'l1','l2','elasticnet',None}` selects the regularization type.
- D ✗ `max_iter` is an upper bound; solvers stop earlier when the `tol` convergence criterion is met (and warn if they hit the limit).

**Adversarial pass (concrete objections looked for):**
- Q3: "A could be argued because the tuple length = number of hidden layers." Rejected: option A says "number of layers in the MLP", and the primary documented semantic is neurons per hidden layer; only one option can be chosen and C is the precise one.
- Q5: "Closed-form OLS predictions are invariant to scaling, so Linear Regression is not impacted." Partially valid, but the stem says "**may be** impacted" and gradient-descent/regularized linear regression clearly is; this is the standard textbook grouping. This is the only question where the intended key could plausibly differ.
- Q8: double-checked the direction of the bootstrap condition in option D – it is indeed inverted (max_samples only applies when bootstrap=True).
- Q9: "ElasticNetCV with l1_ratio=0 is ridge." Rejected as the intended reading: the question is about tuning *Ridge Regression*; ElasticNetCV fits a different estimator.
- All "incorrect / always / exactly / may be" trigger words were re-read before finalising.

# Final answers

| Q | Answer |
|---|---|
| 1 | **B** – reduces model complexity |
| 2 | **D** – "NB always outperforms logistic regression" is the incorrect statement |
| 3 | **C** – number of neurons in each hidden layer |
| 4 | **B** – influence of each estimator on the prediction |
| 5 | **A, C** – Linear Regression, SVM |
| 6 | **A, C** |
| 7 | **C, D** – Information Gain, Gini Impurity |
| 8 | **A, B, C** |
| 9 | **A, C** – GridSearchCV, RandomizedSearchCV |
| 10 | **B, C** |

**Confidence:**
- Q1, Q2, Q4, Q6, Q7, Q8, Q10 – **High** (each option checked individually against the scikit-learn documentation/definitions; multiple reasoning passes agreed; no concrete objection survived).
- Q3, Q9 – **High/Medium** (one distractor each – A in Q3, B in Q9 – is arguable only under a loose reading; the precise reading gives the stated answer).
- Q5 – **Medium**: answer follows the standard "scaling affects gradient-based and distance-based methods, not trees or Naive Bayes" grouping, but plain closed-form OLS predictions are scale-invariant, so if your course material stresses that point the key might list only SVM. Double-check your lecture notes on feature scaling.

Verified in a single context (no subagents, no code execution), by per-option checking against documented scikit-learn behaviour and separate re-derivation passes.
