# Algorithm Runtimes (In Progress) 

Feel free to add if encountered 
* {} denotes subscript 
* ^ denotes superscript 
* If not log base is present, assume log base === 2 

## Asymtotic Notations 
Here is just a brief touch on asymtotics </br>
### Given functions f and g 

|  Asymtotic | Rough Meaning | Notation | Note
| ------------- | ------------- | ------------- | ------------- |
|  Oh           |  f <= g   |       |  f is less than or equal to g     |
|  Omega        |  f >= g   |       |  f is greater than or equal to g | 
|  Theta        |  f = g    |       |  f is equal to g     | 
|  Little Oh    |  f < g    |       |  f is strictly less than  g  |
|  Little Omega | f > g     |       |  f is strictly greater than  g    | 

## Integer Multiplication Algorithms 

| Algorithm  | Runtime | Note 
| ------------- | ------------- | ------------- |
|  Karastuba    | O((n ^ (log{2}(3))) ~ (n ^ (1.585))) |               |
|  Strassen     | O((n ^ log(7))) ~ (n ^ (2.807)))     |               | 


## Graph Algorithms

| Algorithm  | Runtime | Data Stucture Implementated | Note 
| ------------- | ------------- | ------------- | ------------- |
| Depth First Search   |  O(V + E)   | Linked list     |
| Flloyd Warshall      | O(N^3)     |               |
| Breadth First Search | O(V + E)    |  Linked List  | Single shortest paths, no weights   |
| Kosaraju             | O(V + E)    |               |
| Topological Sort     | O(V + E)     | Linked List            |
| Edmonds Karp         | O(V * E^2)  |               |

## Greedy Algorithms

| Algorithm  | Runtime |  Data Sturcture Implemented |Note 
| ------------- | ------------- | ------------- |
| Dijkstra            | O(E +(V * log(V)) | Fibonacci Heap | Assumes all weights are positive|
| Prim                | O((N + M) * log(n))  | Binary heap |                               |
| Kruskal             | O(E * log E)  |  Union-Find  |          | 
| Bellman Ford        | Content       |               | Allows negative weights, no negative cycles |
| Ford Fulkerson      | Content       |               |         |
| Wildest Paths/Bottleneck    |               |   Content  |   |             
| Edmonds Karp        | O(V * E^2)    |               |             | 

** Note Graph Algorithms may differ in run time dependending the Data structure used.
For instance if implemented with a matrix, access time is O(1), however, O(n^2) space
is used. On the other hand, if implemented with a linked list, access time is at most 
O(n + m) and the space complexity is O(n + m). 

## Sorting Algorithms 

| Algorithm  | Runtime | Note 
| ------------- | ------------- | ------------- |
| Radix Sort      | O(n * k)        |               |
| Merge Sort      | O(n * log(n))   |               |
| Insertion Sort  | O(n^2)          |               |
| Selection Sort  | O(n^2)          |               |
| Counting Sort   | O(n + k)        |               |
| Heap Sort       | O(n * log(n))   |               |
| Quick Sort      | theta(n * log(n)) |               |
| Bucket Sort     | theta(n + k)    |               |

## Master Theorom (Recurrences)




