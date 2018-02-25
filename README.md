# Algorithm Runtimes (In Progress) 

Feel free to add if encountered 
* {} denotes subscript 
* ^ denotes superscript 
* If not log base is present, assume log base === 2 

## Integer Multiplication Algorithms 

| Algorithm  | Runtime | Note 
| ------------- | ------------- | ------------- |
|  Karastuba    | O((n ^ (log{2}(3))) ~ (n ^ (1.585))) |               |
|  Strassen     | O(n ^ log(7)) ~ (n ^ (2.807)))        |               | 


## Greedy/Graph Algorithms


| Algorithm  | Runtime | Note 
| ------------- | ------------- | ------------- |
| Dijkstra           | Content   |               |
| Prim               | Content   |               |
| Kruskal            | Content   |               |
| Depth First Search |  O(V + E) | Linked list runtime representation        |
| Flloyd Warshall    | Content   |               |
| Breadth First Search | O(V + E)  | Single shortest paths, no weights              |
| Bellman Ford        | Content | Allows negative weights, no negative cycles |
| Ford Fulkerson      | Content  |               |
| Wildest Paths/Bottleneck       | Content  |               |
| Kosaraju             | Content  |               |
| Topological Sort    | Content |               |
| Edmonds Karp      | O(V * E^2)  |               |

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




