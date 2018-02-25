# Algorithm Runtimes (In Progress) 

Feel free to add if encountered 
* {} =  denotes subscript 
* ^ = denotes superscript </br>
If not log base is present, assume log base === 2 

## Integer Multiplication Algorithms 

| Algorithm  | Runtime | Note 
| ------------- | ------------- | ------------- |
|  Karastuba    | O((n ^ (log{2}(3))) ~ (n ^ (1.585))) |               |
|  Strassen     | Content Cell  |               | 


## Greedy/Graph Algorithms


| Algorithm  | Runtime | Note 
| ------------- | ------------- | ------------- |
| Dijkstra           | Content   |               |
| Prim               | Content   |               |
| Kruskal            | Content   |               |
| Depth First Search |           |               |
| Flloyd Warshall    | Content   |               |
| Breadth First Search | Content  |               |
| Bellman Ford        | Content | Allows negative, no negative cycles |
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
| Radix Sort    | Content  |               |
| Bucket Sort    | Content |               |
| Cyborg Sort    | Content |               |
| Merge Sort     |   O(n * log(n))     |               |
| Insertion Sort  | Content |               |
| Selection Sort  | Content |               |
| Counting Sort   | Content |               |
| Heap Sort      | Content |               |
| Quick Sort     | Content |               |

## Master Theorom (Recurrences)




