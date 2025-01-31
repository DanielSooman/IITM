1) The following pseudocode is executed using the “Words” dataset. What will A represent at the end of the execution? **1 point**

```
A = 0
while(Table 1 has more rows){
  Read the first row X in Table 1
  i = 1, B = False
  while(i <= X.LetterCount){
    if(ith letter of X.Word followed by a vowel){
      B = True
    }
    i = i + 1
  }
  if(B){
    A = A + 1
  }
  Move X to Table 2
}
```

- [ ] Number of words with at most one letter followed by a vowel
- [ ] Number of words with exactly one letter followed by a vowel
- [ ] Number of words without any letters followed by a vowel
- [x] Number of words with at least one letter followed by a vowel

2) The following pseudocode is executed using the “Olympics” dataset. What will E represent at the end of the execution? Assume that none of the players have won more than one medal. **1 point**
<hr><hr>
E = 0
1 while(Table 1 has more rows){
2 Read the first row P in Table 1
3 Move P to Table 2
4 while(Table 1 has more rows){
5 Read the first row Q in Table 1
6 if(findDuo(P, Q)){
7 E = E + 1
8 }
9 Move Q to Table 3
10 }
11 Move all rows from Table 3 to Table 1
12 }
13 Procedure findDuo(P, Q)
14 if(P.Country == Q.Country and P.Medal != Q.Medal){
15 return(True)
16 }
17 else{
18 return(False)
19 }
20 End findDuo
21

○ Number of players from the same country with different medals

○ Number of players from different countries with the same medals

● Number of pairs of players from the same country with different medals

○ Number of pairs of players from different countries with the same medals

3) The following pseudocode is executed using the “Library” dataset. Assume that all authors have distinct names 1 point and each book is written by a single author.
<hr><hr>
A = 1, N = 0, count = 0, value = 0
    while(Table 1 has more rows){
        Read the first row X in Table 1
        Move X to Table 2
        while(Table 1 has more rows){
            Read the first row Y in Table 1
            if(X.Author == Y.Author){
                A = A + 1
                Move Y to Table 2
            }
            else{
                Move Y to Table 3
            }
        }
        if(A > N){
            N = A
        }
        A = 1
        count = count + 1
        Delete all rows of Table 2
        Move all rows from Table 3 to Table 1
    }

What will N represent at the end of execution?

- [ ] Maximum number of books published by an author
- [ ] Maximum number of books published by a pair of authors
- [ ] Maximum number of books published by an author in a year
- [x] Maximum number of books published by a pair of authors in a year

4) What will count represent at the end of execution? **1 point**

- [x] Total number of books
- [ ] Number of authors
- [ ] Number of books of same genre
- [ ] Number of authors who wrote books of same genre

5) The given pseudocode is executed using the “Shopping Bills” dataset. frac stores the ratio of the number of customers who purchased both “Soap” and “Facewash” to the number of customers who purchased “Facewash”. Choose the correct code fragment to complete the pseudocode. (Assume there is at least one customer who has purchased “Facewash”).

**1 point**
<hr><hr>
mCount = 0, bCount = 0
while (Pile 1 has more cards){
  Read the top card X in Pile 1
  ********************
  * Fill the code *
  ********************
  Move X to Pile 2.
}
frac = bCount / mCount

Procedure isItem (Y, A)
  C = False
  while (Card Y has more items){
    Read an item Z from ItemList of card Y
    if (Z.Item == A) {
      C = True
    }
    Remove Z from ItemList of Y
  }
  return (C)
End isItem

if (isItem(X, “Facewash”)){
  mCount = mCount + 1
}
if (isItem(X, “Soap”)){
  bCount = bCount + 1
}

if (isItem(X, “Soap”)){
  bCount = bCount + 1
  if (isItem(X, “Facewash”)){
    mCount = mCount + 1
  }
}

if (isItem(X, “Facewash”) and isItem(X, “Soap”)){
  mCount = mCount + 1
  bCount = bCount + 1
}
<hr><hr>
6) The following pseudocode is executed using the “Words” dataset. What will count represent at the end of execution? **1 point**

```
count = 0
while(Table 1 has more rows){
  Read the first row X in Table 1
  Move X to Table 2
  while(Table 1 has more rows){
    Read the first row Y in Table 1
    if(customCheck(X) and customCheck(Y)){
      count = count + 1
    }
    Move Y to Table 3
  }
  Move all rows from Table 3 to Table 1
}
Procedure customCheck(P)
  A = 0, i = 1
  B = False, Flag = False
  while(i <= P.LetterCount){
    if(ith letter of P.Word is a consonant){
      if(B){
        A = 1
      }
      B = True
    }
    else{
      B = False
    }
    i = i + 1
  }
  if(A == 1){
    Flag = True
  }
  return(Flag)
End customCheck
```

- [ ] Number of pairs of words with exactly two consonants
- [ ] Number of pairs of words with at least two consonants
- [x] Number of pairs of words with exactly two consecutive consonants
- [ ] Number of pairs of words with at least two consecutive consonants

7) Two words are said to be conjugate if they fulfill following conditions: **1 point**
<hr><hr>
Number of vowels are same in both the words  
Number of consonants are same in both the words  
The given pseudocode is executed using the “Words” dataset. The variable **count** in the given pseudocode counts the number of conjugate pairs. But the pseudocode may have mistakes in one or more lines. Identify all such lines (if any). Assume that all statements not listed in the options below are free of errors. It is a Multiple Select Question.

```
count = 0
while(Table 1 has more rows){
  Read the first row X in Table 1
  Move X to Table 2
  while(Table 1 has more rows){
    Read the first row Y in Table 1
    if(X.LetterCount == Y.LetterCount){
      if(vCount(X) == vCount(Y)){
        count = count + 1
      }
    }
    Move Y to Table 3
  }
  Move all rows from Table 3 to Table 1
}
Procedure vCount(Z)
  vowelCount = 0, i = 0
  while(i <= Z.LetterCount){
    if(ith letter of Z.word is a vowel){
      vowelCount = vowelCount + 1
    }
    i = i + 1
  }
  return(vowelCount)
End vCount
```

- [ ] Line 8: Invalid parameter is used to call the procedure inside the conditional statement

- [ ] Line 8: Incorrect condition to update **count** as the number of consonants are not being compared

- [ ] Line 17: Incorrect initialization of **vowelCount**

- [ ] Line 17: Incorrect initialization of **i**

- [ ] No mistake

8) The following pseudocode is executed using the “Scores” dataset. A student can join a subject club if his/her **1 point** subject score is above the score mentioned. The variables M, P and C store the number of students in Mathematics, Physics and Chemistry clubs respectively.
<hr><hr>
M = 0, P = 0, C = 0
while(Table 1 has more rows){
  Read the first row X in Table 1
  subject = maxSubject(X)
  if(subject == "Mathematics" and X.Mathematics > 95){
    M = M + 1
  }
  if(subject == "Physics" and X.Physics > 90){
    P = P + 1
  }
  if(subject == "Chemistry" and X.Chemistry > 90){
    C = C + 1
  }
  Move X to Table 2
}
Procedure maxSubject(Z)
  if(Z.Physics > Z.Mathematics){
    if(Z.Physics > Z.Chemistry){
      return("Physics")
    }
    else{
      return("Chemistry")
    }
  }
  else{
    if(Z.Mathematics > Z.Chemistry){
      return("Mathematics")
    }
    else{
      return("Chemistry")
    }
  }
End maxSubject

Which club can a student join if he/she gets 92 marks in Physics and Mathematics but 84 in Chemistry?

- [ ] Physics club
- [ ] Chemistry club
- [ ] Mathematics
- [x] The student cannot join any club

9) When can a student join more than one club?

1 point

- [x] If the student gets more than 90 marks in at least two subjects
- [ ] If the student gets more than 90 marks in Physics and Chemistry
- [ ] If the student gets more than 90 marks and the same marks in Physics and Chemistry
- [ ] A student cannot join more than one club
<hr><hr>
10) The following pseudocode is executed using the “Words” dataset. What will A represent at the end of execution?

1 point

```plaintext
A = 0, B = 0
P = True, Q = False
while (Table 1 has more rows){
  Read the first row X in Table 1
  if (X.PartofSpeech == "Adverb" and P){
    P = False
    Q = True
  }
  else{
    if (not Q){
      A = A + 1
    }
  }
  if (X.word ends with a full stop){
    P = True
    Q = False
  }
  Move X to Table 2
}
```

- Number of adverbs before the first adverb in every sentence
- Number of words after the first adverb in every sentence
- Number of words before the first adverb or full stop in every sentence
- Number of adjectives before the first adverb in every sentence
- Number of words before the first adverb in every sentence
