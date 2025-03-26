
1)
An undirected graph G has 46 vertices and the degree of each vertex is at least 5. What is the minimum number of edges that the graph G can have?  

---

2)  
If G is a connected undirected graph such that every vertex has degree at most 9, and the shortest path between any two vertices has length at most 2, then what is the maximum number of vertices in G?  
*(Hint: Try to draw the BFS tree starting with any vertex)*  


---

3)  DIY
---

Question 4  

Suppose **G** is a graph with 6 vertices {0, 1, 2, 3, 4, 5} and the adjacency matrix of the graph **G** is:  

<table>
<tr>
<td>
0
</td>
<td>
0
</td>
<td>
1
</td>
<td>
0
</td>
<td>
0
</td>
<td>
1
</td>
</tr>
<tr>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
1
</td>
</tr>
<tr>
<td>
0
</td>
<td>
0
</td>
<td>
1
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
</tr>
<tr>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
</tr>
<tr>
<td>
1
</td>
<td>
1
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
</tr>
<tr>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
<td>
0
</td>
</tr>
</table>

Which of the following statements is True?  

☐ The graph **G** is a directed acyclic graph.  
☐ From vertex 4, every other vertex is reachable.  
☐ The longest path in the graph **G** has length 4, in terms of number of edges.  
☐ The longest path in the graph is 4 → 0 → 2 → 3.  

---

# USE THE FOLLOWING INFORMATION FOR QUESTIONS [5-6]:  

Shreya needs to perform 10 tasks namely {**A, B, C, D, ... J**}. Some tasks need to be performed after performing a particular task. In the below table, column 1 shows the tasks and column 2 shows the sets of tasks that can be performed only after performing the particular task.  

<table>
<thead>
<tr>
<th>Task</th>
<th>Tasks that can be performed after</th>
</tr>
</thead>
<tbody>
<tr>
<td>A</td>
<td>{B, C}</td>
</tr>
<tr>
<td>B</td>
<td>{D}</td>
</tr>
<tr>
<td>C</td>
<td>{E, F}</td>
</tr>
<tr>
<td>D</td>
<td>{G}</td>
</tr>
<tr>
<td>E</td>
<td>{H}</td>
</tr>
<tr>
<td>F</td>
<td>{I}</td>
</tr>
<tr>
<td>G</td>
<td>{J}</td>
</tr>
<tr>
<td>H</td>
<td>{}</td>
</tr>
<tr>
<td>I</td>
<td>{}</td>
</tr>
<tr>
<td>J</td>
<td>{}</td>
</tr>
</tbody>
</table>
<hr><hr>
### Task Dependencies Table

| Task | Dependencies       |
|------|--------------------|
| A    | {B, E, G}          |
| B    | {F, H}             |
| C    | {E, F, I}          |
| D    | {F, I}             |
| E    | {G}                |
| F    | {H, J}             |
| G    | {J}                |
| H    | {G, J}             |
| I    | {J}                |
| J    | {}                 |

---

Question 5  
Which of the following sequences may represent the possible order in which Shreya can perform the tasks?

☐ A, C, B, D, E, I, F, H, G, J  
☐ A, D, C, B, E, I, F, H, G, J  
☐ C, A, D, E, B, I, F, G, H, J  
☐ D, C, A, B, E, I, F, H, G, J  

---

Question 6  
If each task takes 5 minutes to complete and she performs all the independent tasks simultaneously, then the time (in minutes) taken by Shreya to complete all the tasks is

---

Question 7  
An undirected weighted graph \( G \) is shown below. Find the set of all positive integer values of \( x \) such that if we use Dijkstra’s algorithm, there will be a unique shortest path from vertex \( a \) to vertex \( j \) that contains the edge \( (b, e) \).


---

### Question 7

A directed graph \( G \) is shown below. Suppose we are trying to perform an algorithm to find the shortest path from vertex \( i \) to \( j \). Which of the following statements is (are) correct?

![Graph Diagram](<logo>Graph<logo>)

#### Options:
☐ \( \{x | x \in \mathbb{Z}, 0 < x < 8\} \)  
☐ \( \{x | x \in \mathbb{Z}, 0 < x < 7\} \)  
☐ \( \{x | x \in \mathbb{Z}, 0 < x < 6\} \)  
☐ \( \{x | x \in \mathbb{Z}, 0 < x < 9\} \)  

---

### Question 8

A directed graph \( G \) is shown below. Suppose we are trying to perform an algorithm to find the shortest path from vertex \( v_0 \) to \( v_4 \). Which of the following statements is (are) correct?

#### Graph Diagram:
<table>
  <tr>
    <td>v0</td>
    <td>10</td>
    <td>v1</td>
    <td>-5</td>
    <td>v2</td>
  </tr>
  <tr>
    <td>v3</td>
    <td>4</td>
    <td>v4</td>
    <td>2</td>
    <td>v5</td>
  </tr>
  <tr>
    <td>v6</td>
    <td>-9</td>
    <td>v7</td>
    <td>8</td>
    <td>v8</td>
  </tr>
</table>

#### Options:
☐ Dijkstra’s algorithm can be used to find the shortest path from \( v_0 \) to \( v_4 \).  
☐ Bellman-Ford algorithm can be used to find the shortest path from \( v_0 \) to \( v_4 \) because there are negative weighted edges.  
☐ The weight of the shortest path from \( v_0 \) to \( v_4 \) is 1.  
☐ Bellman-Ford algorithm cannot be used to find the shortest path from \( v_0 \) to \( v_4 \) because there is a negative cycle in the given graph.  

<page_number>1 point<page_number>
<hr><hr>
### 9) Which of the following statements is (are) INCORRECT?  
☐ In an undirected graph \( G \), if all edges have different positive weights, then the minimum cost spanning tree of graph \( G \) is unique.  
☐ If there is a cycle of weight 0 in a directed graph \( G \), then we cannot find the shortest path using Bellman-Ford algorithm.  
☐ Suppose an acyclic undirected graph \( G \) with \( n \) vertices has \( n - 1 \) edges. Then the graph is connected.  
☐ In a graph \( G \), every edge with the minimum weight will be in the minimum cost spanning tree.  

---

### (Use the following information for questions 10 & 11)  
A company has branches in each of six cities \( C_0, C_1, ..., C_5 \). The fare (in thousands of rupees) for a direct flight from \( C_i \) to \( C_j \) is given by the \( (i, j) \)-th entry in the following matrix (\( \infty \) indicates that there is no direct flight):  

<table>
  <tr>
    <td>0</td>
    <td>5</td>
    <td>∞</td>
    <td>∞</td>
    <td>4</td>
    <td>8</td>
  </tr>
  <tr>
    <td>5</td>
    <td>0</td>
    <td>3</td>
    <td>10</td>
    <td>∞</td>
    <td>∞</td>
  </tr>
  <tr>
    <td>∞</td>
    <td>3</td>
    <td>0</td>
    <td>11</td>
    <td>∞</td>
    <td>∞</td>
  </tr>
  <tr>
    <td>∞</td>
    <td>10</td>
    <td>11</td>
    <td>0</td>
    <td>4</td>
    <td>∞</td>
  </tr>
  <tr>
    <td>4</td>
    <td>∞</td>
    <td>∞</td>
    <td>4</td>
    <td>0</td>
    <td>3</td>
  </tr>
  <tr>
    <td>8</td>
    <td>∞</td>
    <td>∞</td>
    <td>∞</td>
    <td>3</td>
    <td>0</td>
  </tr>
</table>

---

### 10) An employee of that company wanted to travel from the city \( C_2 \) to the city \( C_5 \). If he travelled by the cheapest route possible, then the total fare (in thousands of rupees) he paid for flight journey was  
☐  

---

### 11) If an inspection team member wanted to inspect all the branches of the company starting from \( C_2 \) and ending at \( C_5 \), visiting each branch exactly once, then which of the following routes should he choose in order to pay minimum fare for flight journey?  
☐ \( C_2 \rightarrow C_3 \rightarrow C_1 \rightarrow C_0 \rightarrow C_4 \rightarrow C_5 \)  
☐ \( C_2 \rightarrow C_1 \rightarrow C_3 \rightarrow C_4 \rightarrow C_0 \rightarrow C_5 \)  
☐ \( C_2 \rightarrow C_3 \rightarrow C_1 \rightarrow C_4 \rightarrow C_0 \rightarrow C_5 \)  
☐ Such a route is not possible.  

---

### (Use the following information for questions 12 & 13)  

<page_number>1 point</page_number>
<hr><hr>
Seven computers {C₀, C₁, C₂, ..., C₆} are linked by a network, and each link has a maintenance cost. The graph below shows how the computers are linked. Each node represents a computer, each edge represents a link between a pair of computers, and weights on the edges represent the maintenance cost (in hundreds of rupees). The goal is to pick a subset of links such that the total maintenance cost is minimum and the computers remain connected through the chosen links.

![Graph Representation]
- Nodes: C₀, C₁, C₂, C₃, C₄, C₅, C₆
- Edges with weights:
  - C₀ ↔ C₁: 2
  - C₀ ↔ C₂: 7
  - C₁ ↔ C₂: 4
  - C₁ ↔ C₄: 1
  - C₂ ↔ C₃: 8
  - C₂ ↔ C₅: 3
  - C₃ ↔ C₆: 5
  - C₄ ↔ C₅: 6
  - C₅ ↔ C₆: 5

---

### 12) What is the total maintenance cost (in hundreds of rupees) of the optimum subset of links?

☐  
☐  
☐  
☐  

**1 point**

---

### 13) Find the number of different ways of choosing an optimum subset of links for the given graph.

☐  
☐  
☐  
☐  

**1 point**

---

### (Use the following information for questions 14 & 15)

Consider a weighted graph G with 7 vertices {A, B, C, D, E, F, G}, which is represented by the following adjacency matrix:


<table>
  <tr>
    <td> </td><td>A</td><td>B</td><td>C</td><td>D</td><td>E</td><td>F</td><td>G</td>
  </tr>
  <tr>
    <td>A</td><td>0</td><td>6</td><td>0</td><td>0</td><td>9</td><td>0</td><td>7</td>
  </tr>
  <tr>
    <td>B</td><td>6</td><td>0</td><td>8</td><td>0</td><td>0</td><td>0</td><td>0</td>
  </tr>
  <tr>
    <td>C</td><td>0</td><td>8</td><td>0</td><td>0</td><td>0</td><td>1</td><td>3</td>
  </tr>
  <tr>
    <td>D</td><td>0</td><td>0</td><td>0</td><td>0</td><td>2</td><td>0</td><td>0</td>
  </tr>
  <tr>
    <td>E</td><td>9</td><td>0</td><td>0</td><td>2</td><td>0</td><td>0</td><td>0</td>
  </tr>
  <tr>
    <td>F</td><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td><td>0</td><td>5</td>
  </tr>
  <tr>
    <td>G</td><td>7</td><td>0</td><td>3</td><td>0</td><td>0</td><td>5</td><td>0</td>
  </tr>
</table>


---

### 14) Suppose we perform Prim’s algorithm on the graph G starting from vertex A to find an MCST. Then the order in which the vertices are added is

☐ A, C, F, G, B, D, E  
☐  
☐  
☐  

**1 point**

---

<page_number>1</page_number>
<hr><hr>
☐ A, B, D, E, G, C, F  
☐ A, B, G, C, F, D, E  
☐ A, C, F, G, E, D, B  

---

**15) Suppose we perform Kruskal’s algorithm on the graph \( G \) starting from vertex \( C \) to find an MCST. Which of the following edges are not added to the minimum cost spanning tree?**  

☐ \( (A, E) \)  
☐ \( (B, D) \)  
☐ \( (G, F) \)  
☐ \( (A, G) \)  

_1 point_  
