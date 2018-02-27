# Algorithm Runtimes (In Progress) 

Feel free to add if encountered 
If there exists CONTENT in a box, it needs Content -- working on it 

* {} denotes subscript 
* ^ denotes superscript 
* If not log base is present, assume log base === 2 

## Asymtotic Notations 
Here is just a brief touch on asymtotics </br>
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
|  Karastuba    | O((n ^ (log{2}(3))) ~ (n ^ (1.585))) |               |
|  Strassen     | O((n ^ log(7))) ~ (n ^ (2.807)))     |  Matrix Multiplication            | 


## Graph Algorithms
 Given a graph G(V,E), V denotes the verticies in a graph and E denotes the edges in a graph 
 </br>
There exists different variations of graphs, i.e graphs can either be directed acyclic, undirected acyclic, directed cyclic, undirected cyclic, residual, and many more ... 
 
 
| Algorithm  | Runtime | Data Stucture | Note 
| ------------- | ------------- | ------------- | ------------- |
| Depth First Search   | O(V + E)   | Linked list    |              | 
| Flloyd Warshall      | theta(V^3)      | Content              |               |
| Breadth First Search | O(V + E)    |  Linked List   | Single shortest paths, no weights   |
| Kosaraju             | O(V + E)    | Linked List               | Run DFS once, then run DFS on the Graph's transpose for SCC's                  |
| Topological Sort     | O(V + E)    | Linked List    | Linked List          |
| Johnson              | O((V^2(log(V)) + (VE))  |   Fibonacci Min Priority Queue     | Uses reweighting technique | 
| Ford Fulkerson       | O(E(F*))  |  Content           | (F*) denotes the maximum flow in a tranformed network     |


## Greedy Algorithms

| Algorithm  | Runtime |  Data Sturcture  | Note 
| ------------- | ------------- | ------------- | ------------- |
| Dijkstra            | O(E(Vlog(V)) | Fibonacci Heap | Assumes all weights are positive|
| Prim                | O((NM)log(N))  | Binary heap |                               |
| Kruskal             | O(Elog(E))  |  Union-Find  |  Runs O((N + M) * log*(n)) with Path Compression (log star(n))| 
| Bellman Ford        | O(VE)       |  Binary heap           | Allows negative weights, no negative cycles |
| Widest Paths/Bottleneck   |  O(Nlog(N)) |   Content  |   |             
| Edmonds Karp        | O(VE^2)    |   Content            |             | 
| Horn Formulae        | O(NM)    |   Content            |  N is number of variables and M is number of formulas  | 
| Huffamn Coding       | O(Nlog(N))    |  Minimum Priority Queue             |   |

** Note Graph Algorithms may differ in run time dependending the Data structure used.
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

## Master Theorom (Recurrences)
In order for the Master Theorom to yield we must have a Recurrence in the form of: 
T(n) =  alpha(T(n/beta)) + gamma*(n^k)
</br>
* where alpha is greater than 1 
* where beta is greater than two
* where gamma and k are positive constants
</br>

T(n) is 
</br>
| Comparison  | Result 
| ------------- | ------------- | 
| alpha > beta^k   | theta(n^(log{beta}(alpha))) |       
| alpha = beta^k   | theta(n^k(log(n)))    |  
| alpha < beta^k   | theta(n^k)| 

| Comparison | Result  | 
| ------------- | ------------- | 
| alpha > beta^k       | theta(n^(log{beta}(alpha)))          |               
| alpha = beta^k        | theta(n^k(log(n)))    |               
| alpha < beta^k  | theta(n^k)           |              
       

## Advanced Data Structures 

#### Dynamic Trees
#### Splay Trees
#### Fusion Trees 
#### Exponential Search Trees 
#### B-Trees
#### Fibonacci Heap
#### van Emde Boas Trees
#### Disjoint Sets
#### y-fast tries 


## Elementary Data Structures 

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



