<details>
  <summary>MLF</summary>

<img width="989" height="565" alt="image" src="https://github.com/user-attachments/assets/a5d30a48-0e73-46ec-a2b1-e4990b2396ae" />
<img width="885" height="352" alt="image" src="https://github.com/user-attachments/assets/0dbe4091-f431-4d1b-8182-583b1f66d02d" />
<img width="832" height="456" alt="image" src="https://github.com/user-attachments/assets/0da3b889-0939-401f-8699-b9345f162f42" />
<img width="762" height="502" alt="image" src="https://github.com/user-attachments/assets/8b1d866a-ff23-467e-ad2a-2df047ba2fa9" />


</details>



---



<details>
  <summary>PDSA</summary>
  <img width="1067" height="306" alt="image" src="https://github.com/user-attachments/assets/d877bb48-9a01-484b-90d4-431c56f19934" />

Minimum Binary
<img width="134" height="65" alt="image" src="https://github.com/user-attachments/assets/3c2a554e-6a3a-4888-8299-c8ff7a31d3cc" />


  
<img width="1023" height="517" alt="image" src="https://github.com/user-attachments/assets/df823a13-1331-4c66-95fc-f350c5eeb4a6" />



Great question! Let me explain **how the tree is built first** — that's what determines the bits! 😊

---

## The Tree is Built by This ONE Rule:
> ### Always combine the 2 SMALLEST frequencies first!

---

## Step by Step — Watch Carefully:

### Starting list (sorted):
```
D=2,  B=5,  C=6,  A=11,  E=12,  F=24
```

---

### Step 1: Take 2 smallest → D(2) and B(5)
```
Combine them → new node = 2+5 = 7

       [7]
      /   \
    D(2)  B(5)
     0      1
```
> D gets 0, B gets 1 (just left=0, right=1)

New list:
```
C=6,  [DB]=7,  A=11,  E=12,  F=24
```

---

### Step 2: Take 2 smallest → C(6) and DB(7)
```
Combine them → new node = 6+7 = 13

        [13]
       /    \
     C(6)  [7]
      0    /   \
         D(2)  B(5)
          0      1
```
> C gets 0, the DB group gets 1

New list:
```
A=11,  E=12,  [CDB]=13,  F=24
```

---

### Step 3: Take 2 smallest → A(11) and E(12)
```
Combine them → new node = 11+12 = 23

       [23]
      /    \
    A(11)  E(12)
      0      1
```

New list:
```
[CDB]=13,  F=24,  [AE]=23
```

---

### Step 4: Take 2 smallest → CDB(13) and AE(23)
```
Combine them → new node = 13+23 = 36

           [36]
          /    \
       [13]    [23]
       /  \    /  \
      C   DB  A    E
      0    1  0    1
```

New list:
```
F=24,  [CDBAЕ]=36
```

---

### Step 5: Last two → F(24) and CDBAЕ(36)
```
Final Tree (ROOT = 60):

              [60]
             /    \
           F(24) [36]
             0   /    \
              [13]    [23]
              /  \    /  \
            C(6) [7] A(11) E(12)
             0   1    0     1
                / \
             D(2) B(5)
              0    1
```

---

## Now Read the Codes:

| Letter | Path from ROOT | Code |
|--------|---------------|------|
| F | Left | **0** |
| C | Right→Left→Left | **100** |
| D | Right→Left→Right→Left | **1010** |
| B | Right→Left→Right→Right | **1011** |
| A | Right→Right→Left | **110** |
| E | Right→Right→Right | **111** |

---

## Why does F get shortest code "0"?
> Because **F had the BIGGEST frequency (24)**, so it got combined LAST → it sits closest to the ROOT → shortest path!

## Why does D get longest code "1010"?
> Because **D had the SMALLEST frequency (2)**, so it got combined FIRST → it sits deepest in tree → longest path!

---

## 🎯 The Golden Rule:
> **Big frequency = combined late = close to root = SHORT code**
> **Small frequency = combined early = deep in tree = LONG code**

Does this clear it up? 😊

<img width="985" height="252" alt="image" src="https://github.com/user-attachments/assets/aba2eae7-98ce-4db4-a696-5cec580147fa" />



<img width="811" height="302" alt="image" src="https://github.com/user-attachments/assets/89d2544d-48fa-4e60-9234-166bb1597cdb" />
<img width="928" height="236" alt="image" src="https://github.com/user-attachments/assets/f9442788-d04a-4411-aaed-9a2e3787eae6" />


<img width="770" height="335" alt="image" src="https://github.com/user-attachments/assets/34bf38b4-a6bb-4f37-89e9-97505e798e3a" />




</details>
























---


<details>
  <summary>DBMS</summary>
<img width="1050" height="245" alt="image" src="https://github.com/user-attachments/assets/3b547f5f-d6f5-47c8-bb4f-c46cf1521754" />

<img width="901" height="568" alt="image" src="https://github.com/user-attachments/assets/beeb0533-7f50-4879-a7f3-d0615dc1c122" />
<img width="803" height="588" alt="image" src="https://github.com/user-attachments/assets/0b178d11-9494-4175-b686-8cb7b5924ce2" />
<img width="790" height="567" alt="image" src="https://github.com/user-attachments/assets/1460a050-37f0-4741-a745-997fe3064693" />

---

<img width="874" height="535" alt="image" src="https://github.com/user-attachments/assets/4ee626bb-7ce6-4567-9275-5573196cadd9" />
<img width="620" height="114" alt="image" src="https://github.com/user-attachments/assets/4aa926ef-a4ea-40a5-b11e-b119388c6484" />
<img width="965" height="370" alt="image" src="https://github.com/user-attachments/assets/638a4cde-50e8-4bad-a280-7ed6db8bf5eb" />


---

<img width="900" height="412" alt="image" src="https://github.com/user-attachments/assets/424bdc65-40d3-402c-97f9-aa97fcf88d13" />



<img width="1096" height="446" alt="image" src="https://github.com/user-attachments/assets/f98a6c75-227d-420d-871d-df1522356946" />
<img width="763" height="331" alt="image" src="https://github.com/user-attachments/assets/80cf0ef9-35c7-4318-94bf-e2107258f04b" />

<img width="1060" height="436" alt="image" src="https://github.com/user-attachments/assets/2546137a-2c05-498b-a115-607f739159cd" />


## Solution

**Given information:**
- Tracks per surface = 128
- Sectors per track = 512
- Bytes per sector = 256
- Minimum bits required to address a sector = 21

---

### Setting Up the Address Structure

To access any sector on the disk, we need to address:

| Field | Value | Bits Required |
|-------|-------|---------------|
| Sector within a track | 512 = 2⁹ | **9 bits** |
| Track (cylinder) | 128 = 2⁷ | **7 bits** |
| Surface (head) | ? | **? bits** |

---

### Calculating Bits for Surface Selection

Total bits = bits for sector + bits for track + bits for surface

$$21 = 9 + 7 + \text{bits for surface}$$

$$\text{Bits for surface} = 21 - 9 - 7 = \boxed{5 \text{ bits}}$$

---

### Finding Number of Platters

- 5 bits → **2⁵ = 32 surfaces**
- Each platter has **2 surfaces**

$$\text{Number of platters} = \frac{32}{2} = \boxed{16 \text{ platters}}$$

---

### ✅ Answer: **16 Platters**

</details>
