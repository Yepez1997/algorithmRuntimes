# Algorithm Runtimes (In Progress) 

Feel free to add if encountered, writing notes on algorithms as I encountered them or have encountered them.
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

## `Asymtotic Notations`
Here is just a brief touch on asymtotics </br>

* Exponential time grows faster then polynomial time 
* Polynomial time grows faster than logarithmic time 
* Logarithmic time grows faster than logarithmic star time (log*(n){grows very very slowly})

### `Given functions f and g` 

|  Asymtotic | Rough Meaning | Notation | Note
| ------------- | ------------- | ------------- | ------------- |
|  Oh           |  f <= g   | f = O(g)            |  f is less than or equal to g     |
|  Omega        |  f >= g   | f = Omega(g)        |  f is greater than or equal to g | 
|  Theta        |  f = g    | f = Theta(g)        |  f is equal to g     | 
|  Little Oh    |  f < g    | f = LittleOh(g)     |  f is strictly less than  g  |
|  Little Omega |  f > g    | f = LittleOmega(g)  |  f is strictly greater than  g    | 

## `Integer Multiplication Algorithms`

| Algorithm  | Runtime | Note 
| ------------- | ------------- | ------------- |
|  Karastuba    | O((n ^ (log{2}(3))) ~ (n ^ (1.585))) |  Python uses Karastuba's Alg. for int multiplication (reducing multiplication calls from 4 -> 3 )   |
|  Strassen     | O((n ^ log(7))) ~ (n ^ (2.807)))     |  Matrix Multiplication            | 
|  Fast Fourier Transform     | theta(n * log(n))   |  Content           | 

## `Graph && Shortest Path Algoriths Algorithms`
 Given a graph G(V,E), V denotes the verticies in a graph and E denotes the edges in a graph. 
 </br>
There exists different variations of graphs, i.e graphs can either be directed acyclic, undirected acyclic, directed cyclic, undirected cyclic, residual, and many more ... 
 
 
| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Depth First Search   | O(V + E)   | Stack   |   Uses stack to keep track of the nodes traversed            | 
| Breadth First Search | O(V + E)    |  Queue   | Single shortest paths, no weights   |
| Kosaraju (SCC'S)            | O(V + E)    | Linked List               | Run DFS once, then run DFS on the Graph's transpose for SCC's                  |
| Topological Sort     | O(V + E)    | Linked List    | Run DFS alpha times -> O(alpha * V + alpha * E) -> O(V + E)        |
| Johnson              | O((V^2(log(V)) + (VE))  |   Fibonacci ... Min Priority Queue     | Uses reweighting technique && all pairs shortest path| 


## `Dynamic Programming`

| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Flloyd Warshall      | theta(V^3)      |  Content         |     All pairs shortest paths          |
| 0-1 KnapSack     | TODO      |  Content         |     0-1 KS ! greedy         |


## `Max-flow/Network Algorithms`
| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Ford Fulkerson       | O(E(F*))  |  Content           | (F*) denotes the maximum flow in a tranformed network     |
| Edmonds Karp        | O(VE^2)    |   Content            |             | 

## `Greedy Algorithms`
Some of these apply to DP problems 
| Algorithm  | Runtime |  Data Sturcture  | Note 
| ------------- | ------------- | ------------- | ------------- |
| Dijkstra            | O(E(Vlog(V)) | Fibonacci Heap | Assumes all weights are positive|
| Prim                | O((NM)log(N))  | Binary heap | Creates Minimum Spanning Tree                              |
| Kruskal             | O(Elog(E))  |  Union-Find  |  Runs O((N + M) * log*(n)) with Path Compression and Union By Rank(log star(n))| 
| Bellman Ford        | O(VE)       |  Binary heap           | Allows negative weights, no negative cycles |
| Widest Paths/Bottleneck   |  O(Nlog(N)) |   Content  |   |             
| Horn Sat Formulae        | O(NM)    |   Linked List            |  N is number of variables and M is number of formulas  | 
| Huffman Coding       | O(Nlog(N))    |  Minimum Priority Queue             |   |
| Set-Cover       | O(klog(N))    |      |  Approximation Algorithm i.e input up to k - otherwise its an np-hard problem | 
| Matroid       | TO DO    |              |   |
| 0-1 Fractional KnapSack     | TODO      |  Content         |    0-1 KnapSack is dp, 0-1 Fractional knapsack IS greedy  |

** Note Graph Algorithms may differ in run time dependending on the Data structure used.
For instance if implemented with a matrix, access time is O(1), however, O(n^2) space
is used. On the other hand, if implemented with a linked list, access time is at most 
O(n + m) and the space complexity is O(n + m). 
** Also the type of data structure used represent a graph can either be a matrix or a table of verticies with collisions - where each collision is an outgoing edge from the vertex. A linked list representation is useful when the graph of the algorithm is sparse - i.e the graph. A sparse graph is defined as a graph whose edges are at most the number of verticies. A dense graph can have more edges per verticies. 

## `Linear Programming`
Simplex

## `Radomized Algorithms` 
#### Las Vegas Algorithms 
#### Monte Carlo Algorithms 

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

## `NP-Complete Algorithms`
| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Set Cover      | Content  |  Content           | Content    |

## `NP-Hard Algorithms`
| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Travelling Salesman Problem     | O(n!)  |  Content           | Using Bruteforce    |
| Bellman/Held/Harp     | O(n^2 * (2^n))  |  Content           | Improvement of TSP using Dynamic Programming    |

## `String Algorithms`
#### Manacher's Algorithm 
#### Knuth Morris Pratt Algorithm (KMP) 


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

 
## `Greedy Algs Notes` 
 
 
## `Dynamic Programming Notes`

## `Advanced Data Structures`
** Will soon implement operations and the cost (running time) for each supported operation for each individual data structure
#### `KD-Trees (Geometric Datastructure)`
#### `Dynamic Tree`s
#### Splay Trees
#### Fusion Trees
| Space  | Runtime | Note |
| ------------- | ------------- | ------------- | 
| theta(n)  | O(log{w}(n)) | assumes we use Word Ram Model, let u = (2^w) 
#### Exponential Search Trees 
#### Fibonacci Heap
#### van Emde Boas Trees
| Space  | Runtime | Note |
| ------------- | ------------- | ------------- | 
| O(log{w}(n)) | O(min(log(w),log{w}(n))) | assumes we use Word Ram Model, let u = (2^w), Store HashTable   |
#### Disjoint Sets
#### Y-fast tries 
#### X-fast tries 
#### B+ Trees
#### B- Trees
#### B Trees
#### Tiered Bit Vectors 
#### Bloomier Filters 


## `Elementary Data Structures` 
** Will soon implement operations and the cost (running time) for each supported operation for each individual data structure. I am familiar with all these !

#### Linked List 
#### Array 
#### Stack
#### Queue 
#### Hash Tables 
#### Binary Search Trees 
#### Red Black Trees
#### AVL Trees 
#### Min/Max Priority Queue
#### Heap
#### Trie Trees 
#### Union Find
#### K-ary heaps 
#### Skip Lists
#### Prefix Tree (Trie)

# Soon to be on here: 
* Multithreaded Algorithms
* Amortized Analysis 
* Möbius inversion
* Linear Programming
* Hashing (Cuckoo Hashing etc etc )
* Semidefinite programming (maybe)

# Other Useful Notes 
* Can sort O(n * sqrt(logn)) using the dynamic fusion trees with the Word Ram Model
 * Can do better with Han's O(n*log(log(n))) or Han and Thorup O(n * sqrt(log(log(n))
* Y-fast Tries make use of X-fast tries and Balanced Binary Search Trees -> theta(n) 
 




