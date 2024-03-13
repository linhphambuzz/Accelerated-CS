### Dijkstra's algorithm 

![](../img/20240301044642.png)

- Dijkstra gives us the shortest path to every vertex 
- SSSE: single source shortest path 
### Edge Cases 
1. Single heavy-weight vs many light-weight path?

![](../img/20240301045312.png)

- Dikstra still finds the shortest path, but took slightly longer 
![](../img/20240301045510.png)

2. Negative edges 
- can't 

3. Undirected graph 
![](../img/20240301045915.png)

### Runing Time Analysis 

O (m + nlog(n))

## Landmark path's problem

![](../img/20240301055010.png)

- In the case if all edges are weighted the same --> use BFS because O(m+n)
![](../img/20240301061420.png)

- Start from L -> make Minimum Spanning Treee
- A->L->G = A->L + L->G = L->A + L->G 