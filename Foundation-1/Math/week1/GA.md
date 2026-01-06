Certainly! Let's go through each question one by one with detailed explanations.

---

### **Question 1: Irrational Numbers**

**Which of the following are irrational numbers?**

- **□ 2.99999999**
- **□ \((\sqrt{8} + \sqrt{2})(\sqrt{12} - \sqrt{3})\)**
- **□ \(\frac{\sqrt{6}}{\sqrt{8}}\)**
- **□ \((\sqrt{8} - \sqrt{2})(\sqrt{18} + \sqrt{2})\)**

**Answer:** 
- \((\sqrt{8} + \sqrt{2})(\sqrt{12} - \sqrt{3})\)
- \(\frac{\sqrt{6}}{\sqrt{8}}\)

**Explanation:**

1. **2.99999999:**
   - This is a terminating decimal (repeating 9s), which is a rational number because it can be expressed as a fraction (e.g., \(2.99999999 = \frac{299999999}{100000000}\)).
   
2. **\((\sqrt{8} + \sqrt{2})(\sqrt{12} - \sqrt{3})\):**
   - Simplify each square root:
     - \(\sqrt{8} = 2\sqrt{2}\)
     - \(\sqrt{12} = 2\sqrt{3}\)
   - Substitute:
     \[
     (2\sqrt{2} + \sqrt{2})(2\sqrt{3} - \sqrt{3}) = (3\sqrt{2})(\sqrt{3}) = 3\sqrt{6}
     \]
   - \(\sqrt{6}\) is irrational, so \(3\sqrt{6}\) is also irrational.

3. **\(\frac{\sqrt{6}}{\sqrt{8}}\):**
   - Simplify:
     \[
     \frac{\sqrt{6}}{\sqrt{8}} = \frac{\sqrt{6}}{2\sqrt{2}} = \frac{\sqrt{3}}{2}
     \]
   - \(\sqrt{3}\) is irrational, so \(\frac{\sqrt{3}}{2}\) is also irrational.

4. **\((\sqrt{8} - \sqrt{2})(\sqrt{18} + \sqrt{2})\):**
   - Simplify each square root:
     - \(\sqrt{8} = 2\sqrt{2}\)
     - \(\sqrt{18} = 3\sqrt{2}\)
   - Substitute:
     \[
     (2\sqrt{2} - \sqrt{2})(3\sqrt{2} + \sqrt{2}) = (\sqrt{2})(4\sqrt{2}) = 8
     \]
   - The result is 8, which is a rational number.

---

### **Question 2: Domain of Function**

**Suppose \(f : D \longrightarrow \mathbb{R}\) is a function defined by \(f(x) = \frac{\sqrt{x^2 - 25}}{x + 5}\), where \(D \subset \mathbb{R}\). Let \(A\) be the set of integers which are not in the domain of \(f\), then find the cardinality of the set \(A\).**

**Answer:** **9**

**Explanation:**

1. **Domain Restrictions:**
   - The expression under the square root must be non-negative:
     \[
     x^2 - 25 \geq 0 \Rightarrow x \leq -5 \text{ or } x \geq 5
     \]
   - The denominator cannot be zero:
     \[
     x + 5 \neq 0 \Rightarrow x \neq -5
     \]
   
2. **Combining the Restrictions:**
   - \(x \geq 5\) or \(x < -5\), but \(x \neq -5\).

3. **Identifying Integers Not in Domain:**
   - All integers between \(-5\) and \(5\) (excluding endpoints where applicable) are not in the domain.
   - Integers not in domain: \(-4, -3, -2, -1, 0, 1, 2, 3, 4\).
   - Total = 9 integers.

---

### **Question 3: Cardinality of Set Difference**

**Consider the set \(S = \{a \mid a \in \mathbb{N}, \ a \leq 21\}\). Let \(R_1\) and \(R_2\) be relations from \(S\) to \(S\) defined as \(R_1 = \{(x, y) \mid x, y \in S, \ y = 3x\}\) and \(R_2 = \{(x, y) \mid x, y \in S, \ y = x^2\}\). Find the cardinality of the set \(R_1 \setminus (R_1 \cap R_2)\).**

**Answer:** **6**

**Explanation:**

1. **Define \(R_1\):**
   - Pairs where \(y = 3x\).
   - Possible \(x\) values where \(3x \leq 21\): \(x = 1, 2, 3, 4, 5, 6, 7\).
   - So, \(R_1\) has 7 pairs.

2. **Define \(R_2\):**
   - Pairs where \(y = x^2\).
   - Possible \(x\) where \(x^2 \leq 21\): \(x = 1, 2, 3, 4\) (since \(5^2 = 25 > 21\)).
   - So, \(R_2\) has 4 pairs.

3. **Intersection \(R_1 \cap R_2\):**
   - Find pairs where \(y = 3x\) and \(y = x^2\).
   - Set \(3x = x^2 \Rightarrow x^2 - 3x = 0 \Rightarrow x(x - 3) = 0\).
   - Solutions: \(x = 0\) (not in \(S\)) and \(x = 3\).
   - Only one pair: \((3, 9)\).

4. **Set Difference \(R_1 \setminus (R_1 \cap R_2)\):**
   - Remove \((3, 9)\) from \(R_1\).
   - Remaining pairs: 6.

---

### **Question 4: Counting Female Tigers**

**In a Zoo, there are 6 Bengal white tigers and 7 Bengal royal tigers. Out of these tigers, 5 are males and 10 are either Bengal royal tigers or males. Find the number of female Bengal white tigers in the Zoo.**

**Answer:** **3**

**Explanation:**

1. **Total Tigers:**
   - Bengal white tigers: 6
   - Bengal royal tigers: 7
   - Total: \(6 + 7 = 13\)

2. **Given:**
   - Males: 5
   - Bengal royal or males: 10

3. **Using Inclusion-Exclusion Principle:**
   - Let \(A\) = Bengal royal tigers, \(|A| = 7\)
   - Let \(B\) = males, \(|B| = 5\)
   - \(|A \cup B| = 10\)
   - \(|A \cap B| = |A| + |B| - |A \cup B| = 7 + 5 - 10 = 2\)

4. **Number of Male Bengal White Tigers:**
   - Total males: 5
   - Males in Bengal royal: 2
   - Thus, males in Bengal white: \(5 - 2 = 3\)

5. **Number of Female Bengal White Tigers:**
   - Total Bengal white tigers: 6
   - Males in Bengal white: 3
   - Females: \(6 - 3 = 3\)

---

### **Question 5: Relations on Ponds**

**A survey was conducted on pollution of 525 ponds across some cities. It was found that 230 ponds are polluted by fertilisers \((F)\), 245 ponds are polluted by pesticides \((P)\) and 257 ponds are polluted by pharmaceutical products \((Ph)\). 100 ponds are polluted by fertilisers and pesticides, 82 ponds are polluted by fertilisers and pharmaceutical products, 77 ponds are polluted by pesticides and pharmaceutical products.**

**Define a relation on the set of 525 ponds such that two ponds are related if both are polluted by fertilisers and pharmaceutical products. Which of the following is/are true?**

- **□ Relation is reflexive.**
- **□ Relation is transitive.**
- **□ Relation is symmetric.**
- **□ This is an equivalence relation.**

**Answer:**
- **Relation is transitive.**
- **Relation is symmetric.**

**Explanation:**

1. **Definition of Relation:**
   - Two ponds \(A\) and \(B\) are related if both are polluted by fertilisers and pharmaceutical products.
   - Formally, \(A \sim B\) if \(A, B \in F \cap Ph\).

2. **Properties:**
   - **Reflexive:** 
     - For all ponds \(A\), \(A \sim A\) must hold.
     - This requires that every pond is polluted by both \(F\) and \(Ph\), which is not true (only \(F \cap Ph\) ponds satisfy).
     - **Not reflexive** unless all ponds are in \(F \cap Ph\), which isn't the case.
   
   - **Symmetric:**
     - If \(A \sim B\), then \(B \sim A\).
     - Since the relation is based on mutual properties, it is **symmetric**.
   
   - **Transitive:**
     - If \(A \sim B\) and \(B \sim C\), then \(A \sim C\).
     - Since all three ponds are in \(F \cap Ph\), \(A \sim C\).
     - Hence, **transitive**.
   
   - **Equivalence Relation:**
     - Requires reflexivity, symmetry, and transitivity.
     - Since reflexivity does not hold, it is **not** an equivalence relation.

---

### **Question 6: Relations Based on Family Tree**

**Mahesh has four sons (Shubh, Rabi, Mahendra, and Rajat). Shubh has two sons (Yashubh and Navrtna). Rabi has two sons named Rathi and Rakesh.**

**Define two relations, R and S, on the set M, which is the collection of all family members, as follows:**

- **\(R := \{(A, B) \mid A \text{ and } B \text{ are cousins, i.e., their parents are siblings}\}\).**
- **\(S := \{(A, B) \mid A \text{ is son of } B\}\).**

**Let \(f := \{(A, B) \mid A \text{ is son of } B\} \subset P \times Q\), where \(P\) and \(Q\) are subsets of M.**

**Which of the following options are correct?**

- **□ f : P → Q is a function, where P = {Yashubh, Navrtna, Rathi, Rakesh, Mahesh} and Q = { Shubh, Rabi, Mahendra, Rajat}.**
- **□ If f : P → Q is a function, where P = { Yashubh, Navrtna, Rathi, Rakesh} and Q = {Shubh, Rabi, Mahendra, Rajat}, then f is one-one.**
- **□ If f : P → Q is a function, where P = {Yashubh, Navrtna, Rathi, Rakesh} and Q = { Shubh, Rabi}, then f is onto.**

**Answer:**
- **If \(f : P \rightarrow Q\) is a function, where \(P = \{ \text{Yashubh, Navrtna, Rathi, Rakesh} \}\) and \(Q = \{ \text{Shubh, Rabi} \}\), then \(f\) is onto.**

**Explanation:**

1. **Understanding \(f\):**
   - \(f\) maps each son to their father.
   - From the family tree:
     - Yashubh and Navrtna are sons of Shubh.
     - Rathi and Rakesh are sons of Rabi.

2. **Option 1:**
   - **\(P = \{Yashubh, Navrtna, Rathi, Rakesh, Mahesh\}\)**
   - **\(Q = \{Shubh, Rabi, Mahendra, Rajat\}\)**
   - Mahesh is included in \(P\), but Mahesh is not a son of anyone in \(Q\).
   - Therefore, \(f\) is **not** defined for Mahesh (he has no father in the set \(Q\)).
   - Hence, \(f\) is **not** a function in this case.

3. **Option 2:**
   - **\(P = \{Yashubh, Navrtna, Rathi, Rakesh\}\)**
   - **\(Q = \{Shubh, Rabi, Mahendra, Rajat\}\)**
   - Each son maps to their respective father:
     - Yashubh → Shubh
     - Navrtna → Shubh
     - Rathi → Rabi
     - Rakesh → Rabi
   - Here, Shubh and Rabi each have two sons mapped to them.
   - Since multiple elements in \(P\) map to the same element in \(Q\), \(f\) is **not** one-one (injective).

4. **Option 3:**
   - **\(P = \{Yashubh, Navrtna, Rathi, Rakesh\}\)**
   - **\(Q = \{Shubh, Rabi\}\)**
   - Each element in \(Q\) is mapped by at least one element in \(P\):
     - Shubh is mapped by Yashubh and Navrtna.
     - Rabi is mapped by Rathi and Rakesh.
   - Therefore, every element in \(Q\) has a pre-image in \(P\), making \(f\) **onto** (surjective).

---

### **Question 7: Further Analysis on Relations R and S**

**(Continuation from Question 6)**

**Which of the following are true?**

- **□ \( R \) is an equivalence relation.**
- **□ (Rathi, Navrtna) ∈ \( R \)**
- **□ \( S \) is an equivalence relation.**
- **□ (Mahesh, Rajat) ∈ \( S \).**
- **□ (Yashubh, Rathi) ∈ \( R \) and (Rathi, Yashubh) ∈ \( R \).**
- **□ \( S \) is symmetric relation.**

**Answer:**
- **\((\text{Rathi}, \text{Navrtna}) \in R\)**
- **\((\text{Yashubh}, \text{Rathi}) \in R\) and \((\text{Rathi}, \text{Yashubh}) \in R\)**

**Explanation:**

1. **\(R\) as an Equivalence Relation:**
   - For \(R\) to be an equivalence relation, it must be reflexive, symmetric, and transitive.
   - **Reflexive:** A person is not a cousin of themselves. Hence, \(R\) is **not reflexive**.
   - **Symmetric and Transitive:** While \(R\) is symmetric and transitive, lacking reflexivity means \(R\) is **not** an equivalence relation.

2. **\((\text{Rathi}, \text{Navrtna}) \in R\):**
   - Rathi is Rabi's son; Navrtna is Shubh's son.
   - Shubh and Rabi are siblings (both are sons of Mahesh).
   - Therefore, Rathi and Navrtna are cousins.
   - Hence, \((\text{Rathi}, \text{Navrtna}) \in R\) is **true**.

3. **\((\text{Yashubh}, \text{Rathi}) \in R\) and \((\text{Rathi}, \text{Yashubh}) \in R\):**
   - Yashubh is Shubh's son; Rathi is Rabi's son.
   - Shubh and Rabi are siblings.
   - Therefore, Yashubh and Rathi are cousins.
   - Since \(R\) is symmetric, both \((\text{Yashubh}, \text{Rathi})\) and \((\text{Rathi}, \text{Yashubh})\) are **true**.

4. **\(S\) as an Equivalence Relation:**
   - \(S\) is defined as "is a son of," which is not reflexive (a person is not their own son), not symmetric (if A is son of B, B is not son of A), and not transitive.
   - Hence, \(S\) is **not** an equivalence relation.

5. **\((\text{Mahesh}, \text{Rajat}) \in S\):**
   - \(S\) relates a son to their father.
   - Mahesh is the father of Rajat, not the son.
   - Hence, \((\text{Mahesh}, \text{Rajat}) \notin S\).

6. **\(S\) is Symmetric:**
   - If \(A\) is son of \(B\), \(B\) is not son of \(A\).
   - Hence, \(S\) is **not** symmetric.

---

### **Question 8: Cardinality of Relations R and S**

**(Continuation from Questions 6 & 7)**

**If \(m\) is the cardinality of the set \(R\) and \(n\) is the cardinality of the set \(S\), then find the value of \(m + n\).**

**Answer:** **16**

**Explanation:**

1. **Cardinality of \(R\) (Cousin Pairs):**
   - \(R\) consists of all unordered pairs of cousins.
   - From the family tree:
     - Cousins are:
       - Yashubh and Rathi
       - Yashubh and Rakesh
       - Navrtna and Rathi
       - Navrtna and Rakesh
     - Total cousin pairs: 4
   - Since \(R\) is symmetric, each pair is represented twice:
     - \((Yashubh, Rathi)\), \((Rathi, Yashubh)\)
     - \((Yashubh, Rakesh)\), \((Rakesh, Yashubh)\)
     - \((Navrtna, Rathi)\), \((Rathi, Navrtna)\)
     - \((Navrtna, Rakesh)\), \((Rakesh, Navrtna)\)
   - Total ordered pairs in \(R\): 8
   - Hence, \(m = 8\).

2. **Cardinality of \(S\) (Son-Father Pairs):**
   - \(S\) consists of all ordered pairs where the first is the son, and the second is the father.
   - From the family tree:
     - Shubh → Yashubh, Navrtna
     - Rabi → Rathi, Rakesh
     - Mahendra and Rajat have no children.
   - Total son-father pairs: 4
   - Hence, \(n = 4\).

3. **Total \(m + n = 8 + 4 = 12\)**

   **Correction:**

   Upon closer inspection, it seems there's an inconsistency in the initial assistant's answer. Based on the detailed explanation:

   - \(m = 8\) (from \(R\))
   - \(n = 4\) (from \(S\))
   - Therefore, \(m + n = 12\)

   However, the assistant previously answered **16**. To align with the correct calculation, the answer should be **12**.

---

### **Question 9: Function Properties**

**Consider the functions \(f : \mathbb{N} \setminus \{0\} \to \mathbb{N} \setminus \{0\}\) and \(g : \mathbb{N} \setminus \{0\} \to \mathbb{N} \setminus \{0\}\) given by:**

\[
f(x) = x + 1
\]

\[
g(x) = \begin{cases} 
f(x) - 1 & \text{if } x > 1, \\
1 & \text{if } x = 1 
\end{cases}
\]

**Which of the following option(s) is(are) true?**

- **[ ] \(f\) is one to one but not onto.**
- **[ ] \(f\) is neither one to one nor onto.**
- **[ ] \(g\) is onto but not one to one.**
- **[ ] \(g\) is a bijective function.**

**Answer:**
- **\(f\) is one to one but not onto.**
- **\(g\) is a bijective function.**

**Explanation:**

1. **Analyzing Function \(f\):**
   - \(f(x) = x + 1\)
   - **One-to-One (Injective):**
     - If \(f(a) = f(b)\), then \(a + 1 = b + 1 \Rightarrow a = b\).
     - Hence, \(f\) is **one-to-one**.
   - **Onto (Surjective):**
     - For \(f\) to be onto, every natural number \(y \geq 1\) must have a pre-image \(x\).
     - However, \(f(1) = 2\), \(f(2) = 3\), etc.
     - The number \(1\) has no pre-image (since \(x \geq 1\), \(f(x) \geq 2\)).
     - Hence, \(f\) is **not onto**.

2. **Analyzing Function \(g\):**
   - Defined as:
     \[
     g(x) = \begin{cases} 
     f(x) - 1 = x & \text{if } x > 1, \\
     1 & \text{if } x = 1 
     \end{cases}
     \]
   - Simplified:
     \[
     g(x) = \begin{cases} 
     x & \text{if } x > 1, \\
     1 & \text{if } x = 1 
     \end{cases}
     \]
   - **One-to-One (Injective):**
     - For \(x > 1\), \(g(x) = x\), which is injective.
     - \(g(1) = 1\), which doesn't duplicate any other output since for \(x > 1\), \(g(x) = x \geq 2\).
     - Hence, \(g\) is **one-to-one**.
   - **Onto (Surjective):**
     - For any \(y \geq 1\), there exists an \(x\) such that \(g(x) = y\):
       - If \(y = 1\), \(x = 1\).
       - If \(y > 1\), \(x = y\).
     - Hence, \(g\) is **onto**.
   - **Bijective:**
     - Since \(g\) is both one-to-one and onto, it is **bijective**.

---

### **Question 10: Function Mapping to Set A**

**Consider the set \(A = \{3k \mid k \in \mathbb{N}\}\). Define a function \(f : \mathbb{N} \to A\), such that \(f(n) = 6n\). Which of the following option(s) is(are) true?**

- **[ ] \(f\) is one to one but not onto.**
- **[ ] \(f\) is neither one to one nor onto.**
- **[ ] \(f\) is onto but not one to one.**
- **[ ] \(f\) is a bijective function.**

**Answer:**
- **\(f\) is one to one but not onto.**

**Explanation:**

1. **Understanding the Sets:**
   - **Domain:** \(\mathbb{N}\) (positive integers: \(1, 2, 3, \dots\))
   - **Codomain:** \(A = \{3, 6, 9, 12, \dots\}\) (multiples of 3)

2. **Function Definition:**
   - \(f(n) = 6n\)
   - Thus, \(f\) maps each natural number to a multiple of 6.

3. **One-to-One (Injective):**
   - If \(f(a) = f(b)\), then \(6a = 6b \Rightarrow a = b\).
   - Hence, \(f\) is **one-to-one**.

4. **Onto (Surjective):**
   - For \(f\) to be onto, every element in \(A\) must have a pre-image in \(\mathbb{N}\).
   - \(A\) includes all multiples of 3, but \(f(n)\) only produces multiples of 6.
   - For example, \(3 \in A\) but there is no \(n\) such that \(6n = 3\) (since \(n\) must be a natural number).
   - Hence, \(f\) is **not onto**.

5. **Conclusion:**
   - \(f\) is **one to one** but **not onto**.

---
