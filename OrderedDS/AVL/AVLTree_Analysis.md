Everything about finding, inserting, removing from a BST remains true
In an AVL tree: 
- extra work on insert/remove 
- stores the height of every node as part of the node itself 
## AVL insert 

![](../img/20240213105002.png)

- Code to check balance of the tree: 

![](../img/20240213112814.png)

- Code to update height and rotate the tree  

![](../img/20240213113027.png)


## AVL:: remove 

- have to find the IOP (right most in left sub- tree) of the node needed to be removed
- rebalance the tree 
- update nodes's height of nodes that's in the path to the node that's removed
![](../img/20240213151718.png)
- In the picture, 5 is swaped with 4 (IOP)
- 2 moved up to fixed the elbow (left rotation) ->(1-2-3) stick
- 2 then moves up again to create the mountain, then whole subtree is reattached to 4 
- finally, update heights. Heights are updated on those nodes that're rearranged for the balance, and path that we took to remove the node
![](../img/20240213152412.png)
- `_iopRemove()` find the IOP on the right most position of left tree
- if IOP is found, swap it with node to be deleted 
- then remove the swapped node. 

## AVL Trees 
- An AVL Tree is an implementation of a balanced BST 
- Implementsyion of an AVL tree starts with a BST implementayion and add 2 keys: 
	- Maintains the hieghts at each node 
	- maintain balance factor after insert and remove 
