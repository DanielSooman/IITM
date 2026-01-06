1)  
Select the correct implementation of a program that accepts a positive integer *x* as input and prints the maximum value of the integer *y* such that \(2^y \leq x\).

**Sample Test Cases**

<table>
  <tr>
    <th><b>Input</b></th>
    <th><b>Output</b></th>
  </tr>
  <tr>
    <td>100</td>
    <td>6</td>
  </tr>
  <tr>
    <td>256</td>
    <td>8</td>
  </tr>
</table>

- [ ] 
  ```python
  x = int(input())
  y = 0
  while x > 1:
      x = x // 2
      y = y + 1
  print(y)
  ```

- [ ] 
  ```python
  x = int(input())
  y = 0
  while x >= 1:
      x = x // 2
      y = y + 1
  print(y)
  ```

- [ ] 
  ```python
  x = int(input())
  y = 0
  while x > 1:
      x = x / 2
      y = y + 1
  print(y)
  ```

- [ ] 
  ```python
  x = input()
  y = 0
  while x > 1:
      x = x // 2
  ```

Option 1

---

2)  
There is a collection of boxes, each box containing certain number of coins. This information is represented as a string such as this: `'|1|4|1|5|9|'`. Here, there are five boxes. The first box has one coin, second has four coins and so on. Assume that each box has at least one coin and at most nine coins. Select the correct implementation of a snippet of code that computes the average number of coins across the boxes and stores it in a variable named `avg`. Assume that the string `boxes` is already given to you and that there is at least one box in the collection.  
Sample initialization of boxes: `'|1|4|1|5|9|'`  
Assume that `boxes` is initialized before.

---

1.
```python
num = 0
total = 0
for i in range(len(boxes)):
    if i % 2 == 0:
        continue
    coins = boxes[i]
    total += coins
    num += 1
avg = total / num
```

2.
```python
num = 0
total = 0
for i in range(len(boxes)):
    if i % 2 == 0:
        continue
    coins = int(boxes[i])
    total += coins
    num += 1
avg = total / num
```

3.
```python
num = 0
total = 0
for coins in boxes:
    total += coins
```
4.
```python

1 num = 0  
2 total = 0  
3 for i in range(len(boxes)):  
4 &nbsp;&nbsp;&nbsp;&nbsp;if i % 2 == 0:  
5 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break  
6 &nbsp;&nbsp;&nbsp;&nbsp;coins = int(boxes[i])  
7 &nbsp;&nbsp;&nbsp;&nbsp;total += coins  
8 &nbsp;&nbsp;&nbsp;&nbsp;num += 1  
9 avg = total / num  
```
Option 2 is correct.  

---

3)
The first five terms of the Fibonacci sequence is given below.  

\( F_1 = 1 \quad F_2 = 1 \quad F_3 = 2 \)  
\( F_4 = 3 \quad F_5 = 5 \)  

We wish to write a program that accepts a positive integer *n* as input and prints \( F_n \) as the output. Select all correct implementations of this program. (MSQ)  

---
```
1 n = int(input())  
2 F_prev = 1  
3 F_curr = 1  
4 count = 2  
5 while count < n:  
6 &nbsp;&nbsp;&nbsp;&nbsp;temp = F_prev + F_curr  
7 &nbsp;&nbsp;&nbsp;&nbsp;F_prev = F_curr  
8 &nbsp;&nbsp;&nbsp;&nbsp;F_curr = temp  
9 &nbsp;&nbsp;&nbsp;&nbsp;count += 1  
10 print(F_curr)  
```
---
```
1 n = int(input())  
2 if n <= 2:  
3 &nbsp;&nbsp;&nbsp;&nbsp;print(1)  
4 else:  
5 &nbsp;&nbsp;&nbsp;&nbsp;F_prev = 1  
6 &nbsp;&nbsp;&nbsp;&nbsp;F_curr = 1
```
---


```python
count = 2
while count < n:
    temp = F_prev + F_curr
    F_prev = F_curr
    F_curr = temp
    count += 1
print(F_curr)
```



```python
n = int(input())
F_prev = 1
F_curr = 1
for i in range(n):
    temp = F_prev + F_curr
    F_prev = F_curr
    F_curr = temp
print(F_curr)
```



```python
n = int(input())
F_prev = 1
F_curr = 1
for i in range(n - 2):
    temp = F_prev + F_curr
    F_prev = F_curr
    F_curr = temp
print(F_curr)
```
Option First and Last
---

4)

If the while loop of below code executes, when does it terminate?

```python
x = int(input("Enter any number: "))
while(x % 5 != 0 and x % 10 != 0):
    x = int(input("Enter any number: "))
print("outside loop, the value of x is ", x)
```

☐ Never terminates it is a infinite loop.

☑ when we input a number which is multiple of 10.

☑y when we input a number which is multiple of 5.

☐ when we input a number which is not a multiple of both 5 and 10.

---

5)
Assume that a ten letter word is passed as input to the code. If the output is `True`, then which of the following statements about the input word are true?###

- ☐ The word has exactly five vowels.

- x The word has have at least five vowels.

- x The letters at even indices are vowels. Assume that we use zero-based indexing.

- ☐ Every vowel in the word appears only at even indices. Assume that we use zero-based indexing.

---

6)
What is the output of the following snippet of code?

```python
alpha = 'abcdefghijklmnopqrstuvwxyz'
shift = 5
word = 'python'
encoded_word = ''  # there is no space between quotes
for char in word:
    shifted_index = (alpha.index(char) + shift) % 26
    encoded_char = alpha[shifted_index]
    encoded_word += encoded_char
print(encoded_word)
```

☐ stmydu
☐ tcxlsr
☐ veznut  
x udymts  
   
---

7) 
What does the following code block print?

```python
for i in 'We are in question one':
    if i == 'a' or i == 'e' or i == 'i' or i == 'o' or i == 'u':
        continue
    print(i, end = '')
```

x W r n qstn n  
☐ Wrnqstnn  
☐ We are in question one  
☐ None of the above  


---
8) 
A programmer wants to print a decreasing sequence. How many times does the `print` statement get executed? And why?

```python
for i in range(10, 0, 1):
    print(i)
```

☐ One time because `i` takes only the value 10 and thereafter it will be decremented  
☐ One time because `i` takes only the value 9 and thereafter it will be decremented  
☐ `print` statement will not be executed due to invalid end points
x `print` statement will not be executed due to incompatible step size

---

 9) 
Which is the correct option that can be used in order to add ‘n-1’ blank spaces after a given string T?  
Note: Variable T is a single character string.

  ○ `print("%ns"%T)`  
  ○ `print("-ns"%T)`  
  x `print("%-ns"%T)`  
  ○ `print("-ns"%T)`


---


10) 
What will be output if a negative value is given as input?

  ○ Number of digits in x  
  ○ Number of digits in x -1  
  ○ Number of digits in x +1  
  x Infinite loop

---

11)  
**Common data for the next 2 questions**  
Consider the following snippet of code.

```
for x in range(100):
    for y in range(100):
        if x != y:
            print(f'{x},{y}')
```
When the code given above is executed, how many lines will the output have? (NAT)
```
9900
```

---

12)
Among the code blocks given below, select the correct equivalent implementation of the code given in the common data.

1.
```python
x, y = 0, 0
while x < 100:
    while y < 100:
        if x != y:
            print(f'{x},{y}')
```

2.
```python
x, y = 0, 0
while x < 100:
    while y < 100:
        if x != y:
            print(x, y)
    x += 1
    y += 1
```

3.
```python
x, y = 0, 0
while x < 100:
    while y < 100:
        if x != y:
            print(x, y)
    y += 1
    x += 1
```

4.
```python
x, y = 0, 0
while x < 100:
    while y < 100:
        if x != y:
            print(x, y)
    y += 1
```
option 2
---

13)  
Select all the snippets that prints the sum of the first n odd numbers starting from 1 (including). Assume n is a positive integer and is already defined.  

Example n = 5, output: 1+3+5+7+9 = 25  

|   | Code Snippet                                                                 |
|---|------------------------------------------------------------------------------|
| ☐ | 1 result = 0                                                                 |
|   | 2 i = 0                                                                      |
|   | 3 while i<n:                                                                 |
|   | 4 &nbsp;&nbsp;&nbsp;&nbsp;result+=2*i+1                                      |
|   | 5 &nbsp;&nbsp;&nbsp;&nbsp;i+=1                                               |
|   | 6 print(result)                                                              |
| ☐ | 1 result = 0                                                                 |
|   | 2 i = 1                                                                      |
|   | 3 while i<n:                                                                 |
|   | 4 &nbsp;&nbsp;&nbsp;&nbsp;result+=2*i+1                                      |
|   | 5 &nbsp;&nbsp;&nbsp;&nbsp;i+=1                                               |
|   | 6 print(result)                                                              |
| ☐ | 1 result = 0                                                                 |
|   | 2 i = 1                                                                      |
|   | 3 while i<n:                                                                 |
|   | 4 &nbsp;&nbsp;&nbsp;&nbsp;result+=2*i+1                                      |
|   | 5 &nbsp;&nbsp;&nbsp;&nbsp;i+=1                                               |
|   | 6 result+=1                                                                  |
<hr><hr>
- [ ] 
  
  result = 0
  i = 0
  while i<n:
      if i%2 != 0:
          result+=2*i+1
      i+=1
  print(result)
  

- [ ] 
  
  result = 0
  i = 0
  while i<2*n+1:
      if i%2 != 0:
          result+=i
      i+=1
  print(result)
  

- [ ] 
  
  result = 0
  i = 0
  while i<2*n+1:
      if i%2 != 0:
          result+=i
      i+=1
  print(result)
  

- [ ] 
  
  result = 0
  i = 0
  while i<2*n+1:
      if i%2 != 0:
          result+=i
      i+=1
  print(result)




The final answer is  1,5  

---

14)  
**Select all the snippets that prints the sum of the first n odd numbers starting from 1 (including). Assume n is a positive integer and is already defined.**

Example n = 5, output: 1+3+5+7+9 = 25

☐  
```python
result = 0
for i in range(n):
    result+=2*i+1
print(result)
```

☑  
```python
result = 0
for i in range(1,n+1):
    result+=2*i-1
print(result)
```

☑  
```python
result = 0
for i in range(1,n):
    result+=2*i+1
result+=1
print(result)
```

☐  
```python
result = 0
for i in range(1,n):
    result+=2*i+1
print(result)
```

☐  
```python
result = 0
for i in range(-1,-n-1,-1):
    result-=2*i+1
print(result)
```

☐  
```python
result = 0
for i in range(1,n+1):
    result+=2*i+1
print(result)
```
The correct snippets are the first, second, third, and fifth ones
---

15) 
Consider the below code.

```
1  n = int(input())
2  value = 0
3  for i in range(n):
4      value+=int(input())*2
5  print(value)
```

Select all the data processing pattern(s) found in the given code.

☐ Aggregation  
☐ Filtering  
☐ Mapping  
☐ None of the above  

---

16)
Consider the below code.


1  n = int(input())
2  value = ""
3  for i in range(n):
4      value+=input()*2+" "
5  print(value)


Select all the data processing pattern(s) found in the given code.

☐ Aggregation  
☐ Filtering  
☐ Mapping  
☐ None of the above

---

17)  
 
Consider the below code.

```python
sentence = input()
for word in words.split():
    if 'a' in word:
        print(word*2)
```

Select all the data processing pattern(s) found in the given code.

☐ Aggregation

☐ Filtering

☐ Mapping

☐ None of the above

---

18)  
  
Consider the below code.

```python
sentence = input()
value = ""
for char in sentence:
    if char in 'aeiou':
        value+=chr(ord(char)+1)
    else:
        value+=chr(ord(char)-1)
print(value)
```

Select all the data processing pattern(s) found in the given code.

☐ Aggregation

☐ Filtering

☐ Mapping

☐ None of the above

---

19)  
 
Consider the below code.


1 sentence = input()
2 value = ""
3 for char in sentence:
4     if char in 'aeiou':
5         value+=chr(ord(char)+1)
6 print(value)


Select all the data processing pattern(s) found in the given code.

☐ Aggregation

☐ Filtering

☐ Mapping

☐ None of the above

---

20)  

Consider the below code.


1 n = int(input())
2 for i in range(n):
3     num = int(input())
4     if len(str(num))<2:
5         print(num*2)


Select all the data processing pattern(s) found in the given code.

☐ Aggregation

☐ Filtering

☐ Mapping

☐ None of the above

21)  
 
Consider the below code.


1  n = int(input())
2  value = None
3  for i in range(n):
4      num = int(input())
5      if len(str(num))<2:
6          value = num
7  print(value)


Select all the data processing pattern(s) found in the given code.

☐ Aggregation

☐ Filtering

☐ Mapping

☐ None of the above

22)   
Consider the below code.


1  n = int(input())
2  value = None
3  for i in range(n):
4      num = len(input())/2
5      if value is None:
6          value = num
7      elif num < value:
8          value = num

Select all the data processing pattern(s) found in the given code.

☐ Aggregation

☐ Filtering

☐ Mapping

☐ None of the above

---

23)    
Consider the below code.


1  n = int(input())
2  values = {}
3  for i in range(n):
4      num = int(input())
5      l = len(str(num))
6      if l not in values:
7          values[l] = set()
8      values[l].add(num)
9  print(values)


Select all the data processing pattern(s) found in the given code.

☐ Aggregation

☐ Filtering

☐ Mapping

☐ None of the above

---

24)   
Consider the below code.

```python
n = int(input())
for i in range(n):
    a = input()
    b = input()
    print(b)
    print(a)
```

Select all the data processing pattern(s) found in the given code.

☐ Aggregation

☐ Filtering

☐ Mapping

☐ None of the above
---
15 to 24: https://chat.qwen.ai/c/c6358cbf-9d3d-4d3e-9ba1-0a0608ec67b5
---

**25)
Consider the below python code.

```python
num = int(input())
i = -num
result = 0
while True:
    if i > 5:
        break
    if i < -5:
        continue
    result += i
    i += 2
print(result)
```

Select all the possible outputs of the above code for any possible valid integer as input.

Hint: To solve this question you might want to try out with different values of num or automate that with another loop with different values for num. What range of values do you use for this automation?

☑ 0
☐ 1
☐ 2
☐ 3
☑ 4
☑ 5
☑ 6
☐ 7
☑ 8
☑ 9
---

26) 
Consider the below python code.

```python
num = int(input())
i = num
result = 0
while True:
    i -= 4
    if i > 10:
        continue
    if i < -10:
        break
    result += i
print(result)
```

Select all the possible outputs of the above code for any possible valid integer as input.

Hint: To solve this question you might want to try out with different values of num or automate that with another loop with different values for num. What range of values do you use for this automation?

☐ 5
☐ 4
☐ 0
☐ -4
☐ -6
☐ -9
☐ -10
☐ -11
☐ -12
☐ -13

answer:
5

0

–4

–9

–10

–12
