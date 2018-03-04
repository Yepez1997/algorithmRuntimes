# Algorithm Runtimes (In Progress) 

Feel free to add if encountered 
</br>
If there exists CONTENT in a box, it needs Content -- working on it 

Algorithms we care about must be 
 1. Efficient (can we do better?)
 2. Correct 
 
Prove algorithm correctness by Induction, Strong Induction, Contrapositive, etc. More importantly for all steps the algorithm must hold, i.e the maintenance of the algorithm. Asking can we do better every time an algorithm is designed is critical. I.e Can we improve the running time? Can we improve the memory consumption ? etc. etc. 

Take a look at: 
* {} denotes subscript 
* ^ denotes superscript 
* If is not log base is present, assume log base === 2 

## Asymtotic Notations 
Here is just a brief touch on asymtotics </br>

* Exponential time grows faster then polynomial time 
* Polynomial time grows faster than logarithmic time 
* Logarithmic time grows faster than logarithmic star time (log*(n){grows very very slowly})

### Given functions f and g 

|  Asymtotic | Rough Meaning | Notation | Note
| ------------- | ------------- | ------------- | ------------- |
|  Oh           |  f <= g   | f = O(g)            |  f is less than or equal to g     |
|  Omega        |  f >= g   | f = Omega(g)        |  f is greater than or equal to g | 
|  Theta        |  f = g    | f = Theta(g)        |  f is equal to g     | 
|  Little Oh    |  f < g    | f = LittleOh(g)     |  f is strictly less than  g  |
|  Little Omega |  f > g    | f = LittleOmega(g)  |  f is strictly greater than  g    | 

## Integer Multiplication Algorithms 

| Algorithm  | Runtime | Note 
| ------------- | ------------- | ------------- |
|  Karastuba    | O((n ^ (log{2}(3))) ~ (n ^ (1.585))) |  Python uses Karastuba's Alg. for multiplication   |
|  Strassen     | O((n ^ log(7))) ~ (n ^ (2.807)))     |  Matrix Multiplication            | 
|  Fast Fourier Transform     | Content   |  Content           | 

## Graph Algorithms
 Given a graph G(V,E), V denotes the verticies in a graph and E denotes the edges in a graph. 
 </br>
There exists different variations of graphs, i.e graphs can either be directed acyclic, undirected acyclic, directed cyclic, undirected cyclic, residual, and many more ... 
 
 
| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Depth First Search   | O(V + E)   | Linked list    |              | 
| Breadth First Search | O(V + E)    |  Linked List   | Single shortest paths, no weights   |
| Kosaraju             | O(V + E)    | Linked List               | Run DFS once, then run DFS on the Graph's transpose for SCC's                  |
| Topological Sort     | O(V + E)    | Linked List    | Linked List          |
| Johnson              | O((V^2(log(V)) + (VE))  |   Fibonacci Min Priority Queue     | Uses reweighting technique && all pairs shortest path| 


## Dynamic Programming

| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Flloyd Warshall      | theta(V^3)      |  Content         |     All pairs shortest paths          |

## Max-flow Algorithms
| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Ford Fulkerson       | O(E(F*))  |  Content           | (F*) denotes the maximum flow in a tranformed network     |
| Edmonds Karp        | O(VE^2)    |   Content            |             | 

## Greedy Algorithms

| Algorithm  | Runtime |  Data Sturcture  | Note 
| ------------- | ------------- | ------------- | ------------- |
| Dijkstra            | O(E(Vlog(V)) | Fibonacci Heap | Assumes all weights are positive|
| Prim                | O((NM)log(N))  | Binary heap | Creates Minimum Spanning Tree                              |
| Kruskal             | O(Elog(E))  |  Union-Find  |  Runs O((N + M) * log*(n)) with Path Compression (log star(n))| 
| Bellman Ford        | O(VE)       |  Binary heap           | Allows negative weights, no negative cycles |
| Widest Paths/Bottleneck   |  O(Nlog(N)) |   Content  |   |             
| Horn Formulae        | O(NM)    |   Linked List            |  N is number of variables and M is number of formulas  | 
| Huffman Coding       | O(Nlog(N))    |  Minimum Priority Queue             |   |

** Note Graph Algorithms may differ in run time dependending on the Data structure used.
For instance if implemented with a matrix, access time is O(1), however, O(n^2) space
is used. On the other hand, if implemented with a linked list, access time is at most 
O(n + m) and the space complexity is O(n + m). 

## Sorting Algorithms 

| Algorithm  | Runtime |
| ------------- | ------------- | 
| Radix Sort      | O(n * k)          |               
| Merge Sort      | O(n * log(n))     |               
| Insertion Sort  | O(n^2)            |               
| Selection Sort  | O(n^2)            |               
| Counting Sort   | O(n + k)          |               
| Heap Sort       | O(n * log(n))     |               
| Quick Sort      | theta(n * log(n)) |               
| Bucket Sort     | theta(n + k)      |   

## NP-Complete Algorithms
| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Set Cover      | Content  |  Content           | Content    |


## String Algorithms 

## Master Theorem (Recurrences)
In order for the Master Theorom to yield we must have a Recurrence in the form of: 
T(n) =  alpha(T(n/beta)) + gamma*(n^k)
</br>
* where alpha is greater than 1 
* where beta is greater than two
* where gamma and k are positive constants

T(n) is :

         

| Comparison  | Runtime |
| ------------- | ------------- | 
| alpha > beta^k   | theta(n^(log{beta}(alpha)))   |               
| alpha = beta^k   | theta(n^k(log(n)))    |               
| alpha < beta^k   | theta(n^k)           |  

 

## Advanced Data Structures 
** Will soon implement operations and the cost (running time) for each supported operation for each individual data structure

#### Dynamic Trees
#### Splay Trees
#### Fusion Trees 
#### Exponential Search Trees 
#### B-Trees
#### Fibonacci Heap
#### van Emde Boas Trees
#### Disjoint Sets
#### Y-fast tries 
#### Link Cut Trees 
#### Precedence Graphs
#### B+ Trees


## Elementary Data Structures 
** Will soon implement operations and the cost (running time) for each supported operation for each individual data structure

#### Linked List 
#### Array 
#### Stack
#### Queue 
#### Hash Tables 
#### Binary Search Trees 
#### Red Black Trees
#### Min/Max Priority Queue
#### Heap
#### Trie Trees 
#### Union Find
#### K-ary heaps 


# Soon to be on here: 
* Multithreaded Algorithms
* Amortized Analysis 
* Schöning's algorithm
* Möbius inversion
* Linear Programming
* Hashing 
* Semidefinite programming (maybe)




