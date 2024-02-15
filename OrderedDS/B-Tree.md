- Goal: is to create a data structure that's going to perform extremely well in both main memory, as well as in on disk, having  minimum of disk seek, or memory seek. 
- The order of a B-Tree is the maximum number of keys that a given node can have, plus one.
## B-Tree insertion 
![](../img/20240213174915.png)

- Example 

![](../img/20240213181049.png)

- B- Tree recursive insert 
![](../img/20240213182823.png)
- 

### B-Tree properties 

![](../img/20240213182459.png)

- a node with 4 keys, has 5 children 
- internal node is always at least half full 
- internal node only split up as soon as  it's full, so when it's splited up, it's half full 
![](../img/20240213184200.png)

### B-Tree Search 
![](../img/20240214065214.png)

- B-tree search code: 

![](../img/20240214202224.png)

- linear search for the key that we're looking for (O(n))
- if not at the current node, then child node will be fetched. (Olog_m(n))