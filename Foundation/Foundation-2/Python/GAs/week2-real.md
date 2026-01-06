1)

**Common data for the next 4 questions**

Consider the below code.

```python
1  a = 5
2  b = "hello"
3  c = a
4  d = a + 5
5  e = b[:d-7]
6  b,e = d,b
7  b,d = c,b
8  f,d = d,e
9  d,b = e,c
10 b,d = f,e
11 del c
```

Try playing around in [this](https://pythontutor.com/) python tutor link for answering the questions.

What is the total number of objects that were referenced by the variables in the given code during the execution?
```
4
```
---

2)

What is the total number of objects that were referenced by the variables in the given code at the end of the execution?
```
3
```

---

3)

What is the total number of variables referring to the same object as variable `b` (including `b`) at the end of the execution of the given code?
```
2
```
---

4)  
**Select the variable(s) that are referring to the same object as `a` at some point of time during the execution of the above code.**

x b  
x c  
☐ d  
☐ e  
☐ f  

---

5)  
**Assume `s` is a `str`, if the output of `print(s)` is Single backslash `\\` and double backslash `\\\\`, then select the possible the value(s) of `s`.**

x `'Single backslash \\\\ and double backslash \\\\\\\\'`  
☐ `'Single backslash \\ and double backslash \\\\'`  
☐ `'Single backslash /\\/\\ and double backslash /\\/\\/\\/'`  
☐ `'''Single backslash \\ and double backslash \\\\'''`  
☐ `"""Single backslash \\ and double backslash \\\\"""`  

---

6)  
**Consider the given code.**

```
1 s = '''
2 name = "XXX"
3 roll = NNN
4 '''
```

Select the equivalent way(s) of defining `s`.

x
```python
s = '\nname = "XXX"\nroll = NNN\n'
```

☐  
```python
s = 'name = "XXX"\nroll = NNN'
```

☐  
```python
s = """
name = \"XXX\"
roll = NNN
"""
```

☐  
```python
s = """
name = "XXX"
roll = NNN
"""
```

☐  
```python
s = (
"\n",
"name = \"XXX\"\n",
"roll = NNN\n",
)
```

☐  
```python
s = (
"\n"
"name = \"XXX\"\n"
"roll = NNN\n"
)
```

☐  
```python
s = (
"\n"
"name = \"XXX\"\n"
"roll = NNN"
)
```

☐  
```python
s = (
"\n",
"name = \"XXX\"\n",
"roll = NNN"
)
```

```
opt 1,4,6
```

7)  
  
Select the string(s) that are equal to `"0.500"`.

☐ f"{0.5:02f}"  
☐ f"{0.5:03f}"  
☐ f"{0.5:03}"  
☐ str(0.5) + "00"  
☐ f"{0.5}00"  
☐ f"0{.5}00"  
☐ f"{0.545:.1f}00"  

**Options 4, 5, 7.**

---

8)  
 
Consider the below code block.

```
1  n_apples = 5
2  n_bananas = 7
3  s = ...
4  print(s)
```

If the output of the code is `5 apples and 7 bananas.`, select the possible expression(s) that can be used for `s`.

☐ s = r"{n_apples} apples and {n_bananas} bananas."  

☐ s = f'{n_apples} apples and {n_bananas} bananas.'

☐  s = f"{n_apples} apples and {n_bananas} bananas."

☐  s = n_apples+" apples and "+n_bananas+" bananas."

☐  s = str(n_apples)+" apples and "+str(n_bananas)+" bananas."

☐  s = str(n_apples)+"apples and"+str(n_bananas)+"bananas."

Answer: 2, 3, 5

---

9)  
Consider the below code block.
```
| 1 | n_apples = 5 
| 2 | apple_price = 5.7   
| 3 | s = ...  
| 4 | print(s) 
```
If the output of the code is `5 kgs of apple cost ₹ 28.50`, select the possible expression(s) that can be used for `s`.

☐  s = f"{n_apples} kgs of apple cost ₹ {n_apples*apple_price}"

☐  s = f"{n_apples} kgs of apple cost ₹ {n_apples*apple_price:0.2f}"

☐  s = f"{n_apples} kgs of apple cost ₹ {n_apples*apple_price:.2f}"

☐  s = n_apples+" kgs of apple cost ₹ "+n_apples*apple_price

☐  s = str(n_apples)+" kgs of apple cost ₹ "+str(n_apples*apple_price)

☐  s = str(n_apples)+" kgs of apple cost ₹ "+str(n_apples*apple_price)+"0"


2, 3, 6


---

10)  
Consider the below code block.

```
| 1 | a,b = "56" |  
| 2 | s = f'{a*3:9}|{b*5:^9}|{a*7:>9}' |
```

What is the value of the variable `s`? Enter the answer as a single quoted string.

```
'555      |  66666  |  5555555'
```


---


11)  
Assume `s` is a `str` variable. What is the type of the expression  
`str(len(s.upper().split())).isdigit()` ?

- ○ int  
- ○ str  
- ○ float  
- ○ list  
- ○ bool  
- ○ NoneType  

---

12)  
Assume `s` is a `str` variable. What is the type of the expression  
`s[:3].upper().split("-")` ?

- ○ int  
- ○ str  
- ○ float  
- x list  
- ○ bool  
- ○ Raises Error

---


13)  
Assume `s` is a `str` variable. What is the type of the expression `s.lower().isapha()`?

- ○ int  
- ○ str  
- ○ float  
- ○ list  
- ☑ bool  
- ○ NoneType  

---

14)  
Assume `s` is a `str` variable. What is the type of the expression `s.islower()`?

- ○ int  
- ○ str  
- ○ float  
- ○ list  
- ☑ bool  
- ○ NoneType  
- ○ Raises Error  

---

15)  
Assume `s` is a `str` variable. What is the type of the expression `list(s)`?
- ☐ int
- ☐ str
- ☐ float
- x list
- ☐ bool
- ☐ NoneType
- ☐ Raises Error

---

16)  
Assume `s` is a `str` variable. What is the type of the expression `s.lower().alpha()`?

- ☐ int
- ☐ str
- ☐ float
- ☐ list
- ☐ bool
- x Raises error

---

17)  
Assume `s` is a `str` variable. What is the type of the expression `s.title().strip`?

- ☐ int
- ☐ str
- ☐ float
- ☐ list
- ☐ bool
- x None of the above

---

18)  
Assume `s` is a `str` variable. What is the type of the expression `s.join(s[0], s[1], s[3])`?

-  int

-  str

-  float

-  list

-  bool

- x  Raises Error

---

19)  
What is the value stored in the variable `x`?
```
| 1 | x = bool(input()) |
```
**Input**
```
| 1 | False |
```

☐ False
x True
☐ Value Error
☐ 'False'

---

20)  
What is the value of the expression `bool('True')`?

☐ True

☐ False

☐ Raises Error

---

21)  
What is the value of the expression `bool(False)`?

☐ True

x False

☐ Raises Error

---

22)  
What is the value of the expression `bool(0.0)`?

☐ True

x False

☐ Raises Error

---

23)    
What is the value of the expression `not None or "2" or 4`?

- x True  
- ○ False  
- ○ None  
- ○ "2"  
- ○ 4  
- ○ Raises Error  

---

24)  
Consider the below code

```python
1 if a:
2     print('a')
3 elif b:
4     print('b')
5 elif c:
6     print('c')
```

Select the possible output(s) of the given code, assuming any possible values for `a`, `b` and `c`.

- ☐ a  
- ☐ b  
- ☐ a
    b
- ☐ a
    c
- ☐ c

  1,2,5
---

25)  
Consider the below code

```python
if a:
    if b:
        if c:
            print('c')
        else:
            print('b')
else:
    print('a')
```

Select the possible output(s) of the given code, assuming any possible values for `a`, `b` and `c`.

x
1 | a  

x  
1 | b  

☐  
1 | b  
2 | a  

☐  
1 | c
2 | b

☐  
1 | c
2 | b
3 | a

---

26)  
Consider the below code

```python
if a:
    if b:
        print('b')
    elif c:
        print('c')
print('a')
```

Select the possible output(s) of the given code, assuming any possible values for `a`, `b` and `c`.

☐  
1 | a  

☐  
1 | b  

☐  
1 | c  

☐  
1 | b  
2 | a  

☐  
1 | b
2 | c

☐  
1 | c  
2 | a  

☐  
1 | b  
2 | c  
3 | a  


1,4,6
---

27)  
Consider the given code.

```
1 if a:
2     if b:
3         print('ab')
4 elif c:
5     print('c')
```

Select the code block(s) that is/are equivalent to the above code.

☐  
```
1 if a or b:
2     print('ab')
3 elif c:
4     print('c')
```

☐  
```
1 if not (not a or not b):
2     print('ab')
3 elif c:
4     print('c')
```

☐  
```
1 if a:
2     if b:
3         print('ab')
4 if c:
5     print('c')
```

☐ 
```
  if a and b:
      print('ab')
  elif c:
      print('c')
  ```

- [x] 
  ```python
  if a and b:
      print('ab')
  if c:
      print('ac')
  ```

- [x] 
  ```python
  if a and b:
      print('ab')
  if c:
      if not(a and b):
          print('c')
  ```

- [x] 
  ```python
  if a and b:
      print('ab')
  if c:
      if not a:
          print('c')
  ```

- [x] 
  ```python
  if a and b:
      print('ab')
  if not a and c:
      print('c')
  ```
2,4,6,8
---

28) 
Select all the code snippet(s) that execute without any error.
- [x] from math import sin, cos, sqrt
- [ ] from math
  math.sin, math.cos
- [ ] import pi from math
- [ ] import * from math

---

29)  
Consider the following snippet of code:

```python
word = input()
match = False
if word.count('(') == word.count(')'):
    if word.count('[') == word.count(']'):
        if word.count('{') == word.count('}'):
            match = True
if match:
    print('PERFECT!')
else:
    print('IMPERFECT!')
```

Select all possible inputs for which this code prints `PERFECT!` as output. (MSQ)

- [x] (a{b[c]})
- [x] abcd
- [x] )(][}{
- [ ] a(db]


---

30)  
Select the correct implementation of a piece of code that accepts a sentence as input and prints the number of words in it. A sentence is just a sequence of words with a space between consecutive words. You can assume that the sentence will not have any other punctuation marks. You can also assume that the input string will have at least one word. Sample test cases follow:

<table>
  <tr>
    <th>Input</th>
    <th>Output</th>
  </tr>
  <tr>
    <td>this is a sentence</td>
    <td>4</td>
  </tr>
  <tr>
    <td>this sentence is not true</td>
    <td>5</td>
  </tr>
</table>

1. 
```python
sentence = input()
space = ' '  # there is a single space between the quotes
num_words = sentence.count(space)
print(num_words)
```

2. 
```python
sentence = input()
space = ' '  # there is a single space between the quotes
num_words = sentence.count(space) + 1
print(num_words)
```

3. 
```python
sentence = int(input())
space = ' '  # there is a single space between the quotes
num_words = sentence.count(space)
print(num_words)
```

4. 
```python
sentence = input()
num_words = len(sentence)
```

option 2

---

31)  
Consider the below code snippet.

```python
s = "abcdefghijklmnopqrstuvwxyz"
a = int(input())
b = int(input())
c = int(input())
d = int(input())
e = int(input())
print(s[-a:-len(s):-3])
print(s[::-b])
print(s[c:0:-3])
print(s[len(s):-d:-3])
print(s[e:-3])
```

For what user input of `a`, `b`, `c`, `d` and `e` (where 0 <= a,b,c,d,e <= len(s)) does the above code snippet print following output? It is a Numerical Answer Type (NAT) question. Enter your input value separated by `,` without any space like: `7,15,0,4,0`


zwtqnkheb
zwtqnkheb
zwtqnkheb
zwtqnkheb
zwtqnkheb


- 1,3,26,26,0
- 1,3,25,26,0
- 1,3,26,0,0
- [x] 1,3,25,0,0

---

32)  
[Exploratory Problem](#): This problem is meant to encourage you to try certain things outside the lectures. Consider the following snippet of code.

```python
a, b, c, d = input()
print(a)
print(b)
print(c)
print(d)
```

What is the output of this code for the following input? Feel free to use the Python interpreter for exploratory questions.

Input:
1234


Options:

1.
|   |   |
|---|---|
| 1 | 1234 |
| 2 | 1234 |
| 3 | 1234 |
| 4 | 1234 |

2. - [x]
|   |   |
|---|---|
| 1 | 1 |
| 2 | 2 |
| 3 | 3 |
| 4 | 4 |

3.
|   |   |
|---|---|
| 1 | 1 |
| 2 | 1 |
| 3 | 1 |
| 4 | 1 |

4.
|   |   |
|---|---|
| 1 | 4 |
| 2 | 4 |
| 3 | 4 |
| 4 | 4 |



33)
**Common data for the next 2 questions**
A word is termed **valid** if the output of the following code is `True` when the word is given as the input to the code. Answer questions (1) and (2) based on this code.

```python
1  word = input()
2  valid = False
3  # both 'a' and 'z' are in lower case
4  if 'a' <= word[0] <= 'z':
5      if word[0] == word[-1]:
6          valid = True
7  print(valid)
```

Select all **valid** words from the options given below. (MSQ)

x  tacit

x  trumpet

x  ease

☐  TrumpeT

☐  TaciT

---

34)  
Going by the code given in the common data, under what conditions can a word be termed **valid**?

○  A word is termed `valid` if it begins with a lower case letter.

○  A word is termed `valid` if its first and last characters are the same.

x A word is termed `valid` if it begins with a lower case letter **AND** its first and last characters are the same.

☐ A word is termed `valid` if it begins with a lower case letter **OR** its first and last characters are the same.
