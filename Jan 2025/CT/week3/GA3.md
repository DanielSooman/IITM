## Questions (1 & 2)

The following pseudocode is executed using the "Words" dataset:

```plaintext
P = 0, Q = 0
while (Table 1 has more rows) {
  Read the first row X from Table 1
  if (X.LetterCount % 2 == 0) {
    P = P + 1
  }
  else {
    if (X.PartOfSpeech == "Adverb") {
      Q = Q + 1
    }
  }
  Move X to Table 2
}
```

1) **What will P represent at the end of execution?** (MCQ) **2 points**

- O Number of words with an even letter count
- O Number of words with an odd letter count
- O Number of adverbs with an even letter count
- O Number of adverbs with an odd letter count

2) **What will Q represent at the end of execution?** (MCQ) **2 points**

- O Number of adverbs with an even letter count
- O Number of adverbs with an odd letter count
- O Number of words with any letter count
- O Number of adverbs with any letter count

3) The following pseudocode is executed using the "Scores" dataset. (MCQ) **2 points**

```plaintext
1 E = True
2 while (Table 1 has more rows) {
3 Read the first row X from Table 1
4 if (X.Gender == 'F') {
5   if (X.Physics < 60 or X.Chemistry < 60 or X.Maths < 60) {
6     E = False
7   }
8 }
9 Move X to Table 2
10 }

At the end of the execution, E will be True if:

- O All female students have scores greater than or equal to 60 in either Physics, Chemistry, or Maths
- O All female students have scores less than 60 in either Physics, Chemistry, or Maths
- O There is at least one female student with scores less than 60 in Physics, Chemistry, or Maths
- O All female students have scores greater than or equal to 60 in Physics, Chemistry, and Maths

4) The following pseudocode is executed using the "Shopping Bills" dataset. The procedure `checkShoppingBills` accepts a card Y and returns True if the minimum total bill amount of shop Y is greater than the average total bill amount of shop Y, otherwise it returns False. Choose the correct code fragments to complete the procedure. This is a Multiple Select Question (MSQ). Note: `MAX_VALUE` represents the maximum bill amount of shop Y.

```plaintext
1 Procedure checkShoppingBills(Y)
2 count = 0, totalAmount = 0, minAmount = MAX_VALUE
3 while (Pile 1 has more cards) {
4 Read the top card X from Pile 1
5 if (X.ShopName == Y.ShopName) {
6 count = count + 1
7 totalAmount = totalAmount + X.TotalBillAmount
8 if (X.TotalBillAmount < minAmount) {
9   minAmount = X.TotalBillAmount
10 }
11 }
12 Move card X to Pile 2
13 }
14 averageAmount = totalAmount / count
15 ********************
16 * Fill the codes *
17 ********************
18 End checkShoppingBills
```

Choose the correct code fragment to complete the procedure:

1. O
```python
if (minAmount >= averageAmount) {
    return (True)
}
return (False)
```

2. O
```python
if (Y.TotalBillAmount > minAmount) {
    return (True)
}
return (False)
```

3. O
```python
if (Y.TotalBillAmount >= minAmount) {
    return (True)
}
else {
    return (False)
}
```

4. O
```python
if (minAmount > averageAmount) {
    return (True)
}
return (False)
```

5) The following pseudocode is executed using the "Scores" dataset. What will **A** represent at the end of execution? (MCQ) **2 points**

```plaintext
A = 0
while (Table 1 has more rows) {
    Read the first row X from Table 1
    B = True
    if (X.Physics >= 60 and X.Chemistry >= 60 and X.Mathematics >= 60) {
        B = False
    }
    if (B) {
        A = A + 1
    }
    Move X to Table 2
}
```

- O Number of students who scored above 60 in all three subjects
- O Number of students who scored below 60 in at least one subject
- O **A** will always be 0
- O Number of students who scored exactly 60 in all three subjects

6) The following pseudocode is executed using the "Scores" dataset. At the end of the execution, the variable **Count** captures the number of students whose total marks are greater than the average (of total marks) of the entire dataset but have scored below the subject average in at least two subjects. Assume that the variable **AvgT** holds the value of the average total marks, and the variables **AvgP**, **AvgC**, and **AvgM** hold the average marks for Physics, Chemistry, and Mathematics respectively. Choose the correct code fragment to complete the pseudocode. This is a Multiple Select Question (MSQ).

```plaintext
1 Count = 0
2 while (Table 1 has more rows) {
3 Read the first row X from Table 1
4 A = False, B = False, C = False, D = False
5 if (X.Total > AvgT) {
6 A = True
7 }
8 if (X.Mathematics < AvgM and X.Physics < AvgP) {
9 B = True
10 }
11 if (X.Physics < AvgP and X.Chemistry < AvgC) {
12 C = True
13 }
14 if (X.Chemistry < AvgC and X.Mathematics < AvgM) {
15 D = True
16 }
17 ************************
18 ** Fill the code **
19 ************************
20 Move X to Table 2
21 }
```

- [ ] 1 if (A and (B or C or D)) {  
      2 Count = Count + 1  
      3 }

- [ ] 1 if (A and (B and C) and (C and D) and (D and B)) {  
      2 Count = Count + 1  
      3 }

- [ ] 1 if (A or (B and C) or (C and D) or (D and B)) {  
      2 Count = Count + 1  
      3 }

- [ ] 1 if (A or (B or C) or (C or D) or (D or B)) {  
      2 Count = Count + 1  
      3 }

7) The following pseudocode is executed using the "Scores" dataset. What will **A** represent at the end of the execution? (MCQ) **2 points**

```plaintext
1 Suma = 0, SumB = 0
2 CountA = 0, CountB = 0
3 A = 0, J = 0, K = 0
4
5 while (Pile 1 has more cards) {
6 Read the top card X from Pile 1
7 if (X.CityTown == "Vellore") {
8 Suma = Suma + X.Total
9 CountA = CountA + 1
10 }
11 if (X.CityTown == "Chennai") {
12 SumB = SumB + X.Total
13 CountB = CountB + 1
14 }
15 Move card X to Pile 2
16 }
17
18 J = Suma / CountA
19 K = SumB / CountB
20
21 while (Pile 2 has more cards) {
22 Read the top card X from Pile 2
23 if (X.CityTown == "Madurai") {
24 if (X.Total > J) {
25 if (X.Total < K) {
26 A = A + 1
27 }
28 }
29 }
30 Move card X to Pile 1
31 }

```

At the end of the execution, **A** represents the number of students from Madurai having total marks:

- O greater than the average marks of students from Vellore but less than that of Chennai
- O greater than the average marks of students from Vellore and Chennai
- O greater than the average marks of students
- O greater than the average marks of students from Chennai

8) The following pseudocode is executed using the "Scores" dataset. At the end of the execution, **A** captures the number of female students who are below average in at least one subject. Assume that the variables **M**, **P**, and **C** hold the average marks for Mathematics, Physics, and Chemistry respectively. The pseudocode may have mistakes. Identify all such mistakes (if any). This is a Multiple Select Question (MSQ).

```plaintext
1 A = 0
2 while (Table 1 has more rows) {
3 B = True
4 Read the first row X from Table 1
5 if (X.Gender == 'F') {
6 if (X.Mathematics < M) {
7 B = False
8 }
9 if (X.Physics < P) {
10 B = True
11 }
12 if (X.C

hemistry < C) {
13 B = False
14 }
15 }
16 if (B) {
17 A = A + 1
18 }
19 Move X to Table 2
20 }
```

- [ ] Line 1: Incorrect initialization of **A**
- [ ] Line 3: Incorrect initialization of **B**
- [ ] Line 7: Incorrect Update of **B**
- [ ] Line 13: Incorrect Update of **B**
- [ ] No error in the code

9) The following pseudocode is executed using the "Scores" dataset. What will **A** represent at the end of the execution? (MCQ) **2 points**

```plaintext
1 A = 0
2 while (Pile 1 has more cards) {
3 Read the top card X from Pile 1
4 A = A + isInSeq(X)
5 Move X to Pile 2
6 }
7
8 Procedure isInSeq(X)
9 if (X.Mathematics > X.Physics) {
10 if (X.Physics < X.Chemistry) {
11 return (1)
12 }
13 }
14 return (0)
15 End isInSeq
```

- [ ] Number of students with highest marks only in Mathematics out of their three subjects' marks
- [ ] Number of students with highest marks only in Mathematics and lowest marks only in Physics
- [ ] Number of students with highest marks only in Chemistry out of their three subjects' marks
- [ ] Number of students with lowest marks only in Physics out of their three subjects' marks

10) The following pseudocode is executed using the "Words" dataset. What will **A** represent at the end of execution? (MCQ) **2 points**

```plaintext
1 SumT = 0, CountT = 0, B = 0
2 while (Table 1 has more rows) {
3 Read the first row X from Table 1
4 CountT = CountT + 1
5 SumT = SumT + X.LetterCount
6 Move X to Table 2
7 }
8 B = SumT / CountT
9 A = 0
10 while (Table 2 has more rows) {
11 Read the first row X in Table 2
12 if (X.Word ends with a comma) {
13 if (X.LetterCount > B) {
14 A = A + 1
15 }
16 }
17 Move X to Table 1
18 }
```

- O Number of words that end with a comma
- O Number of words that end with a comma and have a letter count greater than the average letter count of the dataset
- O Number of words that end with a comma and have a letter count less than or equal to the average letter count of the dataset
- O Number of words that end with a comma and have a letter count greater than the average letter count of the dataset

