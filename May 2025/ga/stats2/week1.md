1) A fair coin is tossed three times. Let \(X\) denote the number of heads obtained and let \(Y\) be defined as:  
\[
Y = \begin{cases} 
0, & \text{if no heads are obtained} \\
1, & \text{if the first head appears on the first toss} \\
2, & \text{if the first head appears in the second toss} \\
3, & \text{if the first head appears in the third toss}
\end{cases}
\]

Choose the correct joint PMF of \(X\) and \(Y\).

<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th>\(Y \backslash X\)</th>
    <th>0</th>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td>1/8</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
    <td>1/8</td>
    <td>1/8</td>
    <td>1/8</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0</td>
    <td>1/8</td>
    <td>2/8</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>0</td>
    <td>1/8</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="5" style="margin-top:20px;">
  <tr>
    <th>\(Y \backslash X\)</th>
    <th>0</th>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td>1/8</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
    <td>1/8</td>
    <td>1/4</td>
    <td>1/8</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0</td>
    <td>1/8</td>
    <td>1/8</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>0</td>
    <td>1/8</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>
<hr><hr>
<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th rowspan="2">Y \ X</th>
    <th colspan="4">X</th>
  </tr>
  <tr>
    <th>0</th>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td>1/8</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
    <td>1/4</td>
    <td>1/4</td>
    <td>0</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0</td>
    <td>1/4</td>
    <td>1/8</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>0</td>
    <td>0</td>
    <td>1/8</td>
    <td>1/8</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th rowspan="2">Y \ X</th>
    <th colspan="4">X</th>
  </tr>
  <tr>
    <th>0</th>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td>1/8</td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
    <td>1/4</td>
    <td>1/4</td>
    <td>0</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0</td>
    <td>0</td>
    <td>1/8</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>0</td>
    <td>0</td>
    <td>1/8</td>
    <td>1/8</td>
  </tr>
</table>

# Answer: Table 2


2) Joint distribution of two random variables *X* and *Y* is given as:

<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th rowspan="2">Y \ X</th>
    <th colspan="2">X</th>
  </tr>
  <tr>
    <th>0</th>
    <th>1</th>
  </tr>
  <tr>
    <td>1</td>
    <td>1/4</td>
    <td>1/8</td>
  </tr>
  <tr>
    <td>2</td>
    <td>1/4</td>
    <td>k</td>
  </tr>
  <tr>
    <td>3</td>
    <td>0</td>
    <td>1/8</td>
  </tr>
</table>

Table 1.1.G: Joint distribution of *X* and *Y*.

Find the value of *f*<sub>Y|X=1</sub>(2).

```
0.5
```

---

3) Akshat draws a card randomly from a well-shuffled pack of 52 cards. If the drawn card is a face card, then he draws two balls randomly from bag A which contains 6 Red, 7 Black and 2 Green balls. If the drawn card is not a face card, then he draws three balls randomly from bag B which contains 8 Red, 10 Black and 2 Green balls. Let two random variables *X* and *Y* are defined as:
\( X = \begin{cases} 
0 & \text{if the drawn card is a face card} \\
1 & \text{if the drawn card is not a face card}
\end{cases} \)

and \( Y \) be the number of Red balls drawn. Find the value of \( f_Y(1) \). Write your answer correct up to two decimal places.
```
0.47
```

---

4) Which of the following options is/are always correct?  

x \( f_{XYZ}(x,y,z) = f_{X|(Y=y,Z=z)}(x) \cdot f_{YZ}(y,z) \)  
☐ \( f_{XY}(x,y) = f_X(x) \cdot f_Y(y) \)  
☐ \( f_{XYZ}(x,y,z) = f_{X|(Y=y,Z=z)}(x) \cdot f_X(x) \)  
☐ \( f_{XYZ}(x,y,z) = f_{X|(Y=y,Z=z)}(x) \cdot f_{Y|(X=x)}(y) \cdot f_X(x) \)

---

5) Two random variables \( X \) and \( Y \) are jointly distributed with joint pmf

\[
f_{XY}(x,y) = a(bx + y),
\]

where \( x \) and \( y \) are integers in \( 0 \leq x \leq 2 \) and \( 0 \leq y \leq 3 \) such that \( P(X \geq 1, Y \leq 2) = \frac{4}{7} \). Find the value of \( f_{XY}(1,1) \). Write your answer correct to two decimal places.
```
0.07
```

---

6) A fair coin is tossed 4 times. Let \( X \) be the total number of heads and \( Y \) be the number of heads before the first tail (If there is no tail in all the four tosses, then \( Y = 4 \)). What is the value of \( f_{Y|X=2}(0) \)? Write your answer correct to two decimal places.
```
0.50
```

---

7) From a group of 6 members of party A, 5 members of party B, and 4 members of party C, a committee of two people is to be selected uniformly at random. Let \( X \) denote the number of party A members and \( Y \) denote the number of party B members on the committee. Find the value of \( f_{XY}(1,1) \). Write your answer correct to two decimal places.
```
0.29
```

---
8) Suppose a fair six sided die is rolled five times independently. Let \(X\) denote the number of times a 1 is obtained and let \(Y\) denote the number of times a 6 is obtained. Find \(\Pr(X=1, Y=1)\). Enter the answer correct to three decimal places.
```
0.165
```

---

9) **Use the following information to answer below two sub questions.**  
Let random variables \(X\) and \(Y\) be uniformly distributed over the set of integers \(x\) and \(y\) satisfying \(-1 \leq y \leq 1, \quad -2 \leq x + y \leq 2.\)  
Find the marginal PMF of \(X\).

○ \(f_X(x) = \begin{cases} \frac{1}{6}, & \text{if } x = -2, -1, 0, 1, 2, 3 \\ 0, & \text{otherwise} \end{cases}\)

x \(f_X(x) = \begin{cases} \frac{1}{15} & \text{if } x = -3, 3 \\ \frac{2}{15} & \text{if } x = -2, 2 \\ \frac{3}{15} & \text{if } x = -1, 0, 1 \\ 0, & \text{otherwise} \end{cases}\)

○ \(f_X(x) = \begin{cases} \frac{1}{6}, & \text{if } x = -3, -2, -1, 1, 2, 3 \\ 0, & \text{otherwise} \end{cases}\)

○ \(f_X(x) = \begin{cases} \frac{3}{15} & \text{if } x = -3, 3 \\ \frac{2}{15} & \text{if } x = -2, 2 \\ \frac{1}{15} & \text{if } x = -1, 0, 1 \\ 0, & \text{otherwise} \end{cases}\)



---

10) Find the marginal PMF of \(Y\).

○ \(f_Y(y) = \begin{cases} \frac{1}{6}, & \text{if } y = -2, -1, 0, 1, 2, 3 \\ 0, & \text{otherwise} \end{cases}\)

x \(f_Y(y) = \begin{cases} \frac{1}{3}, & \text{if } y = -1, 0, 1 \\ 0, & \text{otherwise} \end{cases}\)

○ \(f_Y(y) = \begin{cases} \frac{1}{6}, & \text{if } y = -3, -2, -1, 1, 2, 3 \\ 0, & \text{otherwise} \end{cases}\)

○ \( f_Y(x) = \begin{cases} 
\frac{1}{3}, & \text{if } y = -2, 0, 2 \\
0, & \text{otherwise}
\end{cases} \)

---

11) **Use the following information to answer the below two sub questions.** *1 point*  
In a classroom, there are three boxes labeled Box 1, Box 2, and Box 3. A teacher places three candies into these boxes, with each candy independently and uniformly likely to go into any box. Let \( X_i \) represent the number of candies in Box \( i \) (\( i = 1, 2, 3 \)), and let \( N \) denote the number of boxes occupied (contain at least one candy).

Obtain the joint distribution of \( (X_1, N) \).

---

(a)

<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th rowspan="2"><em>X</em><sub>1</sub></th>
    <th colspan="3"><em>N</em></th>
  </tr>
  <tr>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td>2/27</td>
    <td>6/27</td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
    <td>2/27</td>
    <td>6/27</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0</td>
    <td>6/27</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>1/27</td>
    <td>0</td>
    <td>4/27</td>
  </tr>
</table>

---

(b)

<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th rowspan="2"><em>X</em><sub>1</sub></th>
    <th colspan="3"><em>N</em></th>
  </tr>
  <tr>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td>2/27</td>
    <td>6/27</td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
    <td>6/27</td>
    <td>6/27</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0</td>
    <td>6/27</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>1/27</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>
<hr><hr>
<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th rowspan="2"><em>X</em><sub>1</sub></th>
    <th colspan="3">N</th>
  </tr>
  <tr>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td>2/27</td>
    <td>5/27</td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
    <td>6/27</td>
    <td>5/27</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0</td>
    <td>8/27</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>1/27</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="5" style="margin-top: 20px;">
  <tr>
    <th rowspan="2"><em>X</em><sub>1</sub></th>
    <th colspan="3">N</th>
  </tr>
  <tr>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td>2/27</td>
    <td>6/27</td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0</td>
    <td>6/27</td>
    <td>5/27</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0</td>
    <td>7/27</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>1/27</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>


---

12) Obtain the joint distribution of \((X_1, X_2)\).  
<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th rowspan="2"></th>
    <th rowspan="2">X<sub>1</sub> \ X<sub>2</sub></th>
    <th colspan="4">0</th>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td><sup>1</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>1</sup>/<sub>27</sub></td>
  </tr>
  <tr>
    <td>1</td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>6</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td>0</td>
  </tr>
  <tr>
    <td>2</td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td><sup>1</sup>/<sub>27</sub></td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>

(a)

<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th rowspan="2"></th>
    <th rowspan="2">X<sub>2</sub> \ X<sub>1</sub></th>
    <th colspan="4">0</th>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td><sup>1</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>1</sup>/<sub>27</sub></td>
  </tr>
  <tr>
    <td>1</td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td>0</td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>6</sup>/<sub>27</sub></td>
  </tr>
  <tr>
    <td>2</td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td><sup>1</sup>/<sub>27</sub></td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>

(b)

<table border="1" cellspacing="0" cellpadding="5">
  <tr>
    <th rowspan="2"></th>
    <th rowspan="2">X<sub>1</sub> \ X<sub>2</sub></th>
    <th colspan="4">0</th>
    <th>1</th>
    <th>2</th>
    <th>3</th>
  </tr>
  <tr>
    <td>0</td>
    <td><sup>1</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>6</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>1</sup>/<sub>27</sub></td>
  </tr>
  <tr>
    <td>2</td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td><sup>3</sup>/<sub>27</sub></td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td><sup>1</sup>/<sub>27</sub></td>
    <td>0</td>
    <td>0</td>
    <td>0</td>
  </tr>
</table>
(c)
- (d). Insufficient information


11) ka B
12) ka A
