## Balanced BST 

- are height-balanced trees that ensures nearly half of the data is located in each subtree
- mountain: node that has both left and right
- Stick: one-sided
![](../img/20240213090431.png)
-  BST insert :  identify deepest node in the tree that's out of balance 

![](../img/20240213092747.png)
###  BST Rotation 
![](../img/20240213093100.png)
- Raise V up
- U is in the left of V 
- Left subtree of U remains untouched
- Right sub-tree of V remains untouched 
- Child node that is left of V, because its value is bigger than U, will attach to right of U
1. Generic left rotation 
![](../img/20240213094411.png)
- Left rotation: bringing `c` up, bring everything to the left 
- This occurs when the deepest point of imbalance has a balanced factor of 2 followed by a point with balanced factor of 1. 
2. Unbend the elbow 
![](../img/20240213095728.png)
- Raise the yellow node up-> transform the elbow to the stick
3. generic right-left rotation 
![](../img/20240213100712.png)
- The process is below: 
![](../img/20240213100607.png)
- going from an elbow, to a stick, to a mountain 

### Rotation Summary
![](../img/20240213103004.png)

-   if b is 2 -> left rotation, is  -2 -> right rotation 
- if followed b, node has sign with b -> only 1 rotation is needed, else 2

![](../img/20240213103819.png)