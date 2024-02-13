1. Access a given index
- Array : O(1)
- List: O(n)
2. Insert
- Array: O(1) amortized constant time when array size is doubled when copied
- List: O(1) fixed constant time by adding new data at head of list
3. Find
- Array: O(n)
- List: O(n)
- Both requires searching up the full array 
4. Find data in sorted array 
- BInary search: O(log2(n))
- List: O(n)
5. Insert after (a given index)
- Array : O(n) . requires copying up to half of the array to remove the blank space
- List: O(1). const time to remove a ListNOde and repair the node