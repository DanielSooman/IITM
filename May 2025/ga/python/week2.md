

1) Which of the following are valid names for variables in Python? (MSQ)  


☑ a_  
☑ _a  
☐ 1a  
☐ a variable  
☑ a_variable  

---

2) Execute the the following code-block. Assume that *word1* and *word2* are strings that have already been defined. **1 point**

```python
# word1, word2 are two strings
print(word1 + word2)
word = word1
word1 = word2
word2 = word
print(word2 + word1)
```

Select the statement that accurately describes the two lines in the output.

- ◉ The two lines are always the same.
- ○ The two lines are always different.
- ○ The two lines are the same if and only if *word1* and *word2* are equal.
- ○ None of the above

---

3) Assume that a, b and c are three distinct integers. The following code runs without any error.  


```python
x, y, z = a, b, c
```
2  x = y = z

Select all statements that evaluate to True at the end of execution of the code given above. (MSQ)

| ☑ | 1 | x == y == z |
|---|---|-------------|
| ☐ | 1 | x == y == z == a |
| ☐ | 1 | x == y == z == b |
| ☑ | 1 | x == y == z == c |

4) x is a variable of type float and is of the form a.bcd, where a, b, c, d are all positive integers less than 10. **1 point**  
What is the output of the following snippet of code?

```python
print(int(x))
print(int(-x))
```

| ☐ | 1 | a     |
|---|---|-------|
|   | 2 | a     |

| ☐ | 1 | a + 1 |
|---|---|-------|
|   | 2 | a + 1 |

| ☐ | 1 | a - 1 |
|---|---|-------|
|   | 2 | a - 1 |

| ☐ | 1 | a - 1 |
2 | -a

- ( )  
  1 | a  
  2 | -a + 1

  - [x]  
  1 | a  
  2 | -a

---

5) Consider the following code blocks:  


**Block-1**

| 1 | flag = True          |  
| 2 | if flag == True:     |  
| 3 | &nbsp;&nbsp;&nbsp;&nbsp;print('works') |

**Block-2**

| 1 | flag = True          |  
| 2 | if flag:             |  
| 3 | &nbsp;&nbsp;&nbsp;&nbsp;print('works') |

Two blocks of code are said to be equivalent if they produce the same output for a given input. Are the two blocks equivalent?

- ( ) Yes  
- ( ) No

---

6) Consider the following code-blocks. E is a Boolean expression. Two blocks of code are said to be equivalent if they produce the same output for a given input.  


**Block-1**

| 1 | if E:                |  
| 2 | &nbsp;&nbsp;&nbsp;&nbsp;print('good') |  
| 3 | else:                |  
| 4 | &nbsp;&nbsp;&nbsp;&nbsp;print('bad')  |

**Block-2**
<hr><hr>
### Code Blocks

```python
if E:
    print('good')
print('bad')
```

**Block-3**

```python
print('good')
print('bad')
```

---

### Select all true statements. (MSQ)

☐ All three blocks are equivalent to each other.

☐ Exactly two of these three blocks are equivalent to each other.

☐ Blocks 1 and 2 print the same output when E evaluates to `True`.

☐ Blocks 1 and 2 print the same output when E evaluates to `False`.

☐ Blocks 2 and 3 print the same output when E evaluates to `True`.

---

7) **bool_var** is a variable of type `bool`. **x** is a variable of type `int`. Assume that both these variables have already been defined. Now, consider the following code-block:

```python
if bool_var:
    x = x + 1
    bool_var = not bool_var
    if bool_var:
        x = x + 1
    else:
        x = x - 1
print(x)
```

---

### Which of the following statements are true at the end of execution of the code-block given above? (MSQ).

☐ The value of variable **x** is independent of the value of **bool_var**.

☐ The value of variable **x** is dependent on the value of **bool_var**.

☐ Line-5 is never executed.

☐ The variable **x** is updated exactly two times.

---

**Common Data for questions (8) and (9)**

Consider the following code-block. E_1, E_2 and E_3 are all Boolean variables that have already been defined. x is a variable that has **NOT** been defined before.

```python
1  if E_1:
2      x = 1
3  if E_2:
4      x = 2
5  if E_3:
6      x = 3
7  print(x)
```

---

8) When will this code throw an error?  

- ○ When all three Boolean variables are `True`.
- ○ When all three Boolean variables are `False`.
- ○ When at least one of the three Boolean variables is `True`.
- ○ When at least one of the three Boolean variables is `False`.
- ○ This code will never throw an error.

---

9) If the code throws an error, in which line will it occur? Enter an integer between 1 and 7, both endpoints included.

---

10) Select the correct code snippet that prints a backslash character to the console.  

- ○  
  ```python
  1 print(\)
  ```
- ○  
  ```python
  1 print('\\')
  ```
- ○
<hr><hr>
1 print('\\')

1 print("\"")


---

11) Consider the following snippet of code:  



1 # Warning! This code may not make complete sense for certain inputs!
2 name = input()
3 if name.isalpha():
4     print('This is a valid name')
5 else:
6     print('This is not a valid name')


If the output of this code is the string `This is a valid name`, select all possible inputs to the program. (MSQ)

☐ 1 Neeraj  
☐ 1 Mirabai  
☐ 1 Sindhu  
☐ 1 X AE A-12  
☐ 1 Rohit Sharma  

---

12) [Exploratory Problem](#): This problem is meant to encourage you to try certain things outside the lectures.  


We have looked at string slicing. Consider the following piece of code:


1 alphabets = 'abcdefghijklmnopqrstuvwxyz'
2 even = alphabets[0: 10: 2]

<hr><hr>
3 print(even)

What is the output? Feel free to use the Python interpreter for exploratory questions.

1 abcdefghij  
○

1 abcde  
○

1 acegi  
○

1 bdfhj  
○

---

13) **Exploratory Problem**: This problem is meant to encourage you to try certain things outside the lectures. 

Consider the following snippet of code.

1 a, b, c, d = input()  
2 print(a)  
3 print(b)  
4 print(c)  
5 print(d)  

What is the output of this code for the following input? Feel free to use the Python interpreter for exploratory questions.

1 1234  

○  
1 1234  
2 1234  
3 1234  
4 1234  

○  
1 1  
2 2  
3 3  
4 4  

○
<hr><hr>
<table>
  <tr>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td>
  </tr>
</table>

<table>
  <tr>
    <td>1</td>
    <td>4</td>
  </tr>
  <tr>
    <td>2</td>
    <td>4</td>
  </tr>
  <tr>
    <td>3</td>
    <td>4</td>
  </tr>
  <tr>
    <td>4</td>
    <td>4</td>
  </tr>
</table>
