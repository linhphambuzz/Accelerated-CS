## puzzle 1 


```
int i = 2, j = 4, k = 8;

int *p = &i, *q = &j, *r = &k;

k = i;

cout << i << j << k << *p << *q << *r << endl;

p = q;

cout << i << j << k << *p << *q << *r << endl;
```


![[Screenshot from 2024-01-27 03-25-47.png]]

```
*q = *r;

cout << i << j << k << *p << *q << *r << endl;
```

![[Screenshot from 2024-01-27 03-28-27.png]]

From the example, note that: 
- All ptr are stack memory
- `i` ,`j`, `k` are int variables, their stack memory are assign to int pointer `p`,`q`,`r`
- first operation: variables swapping values, only `k` changes
- second operation: `p` is assigned to point to what `q` is pointing to, therefore `*p` changes
- third operations: value that `r` is pointing to (i,e:2) is assign to value that `q` is pointing to(i.e:`j`), there fore `*q` and  `j` both changes 
-

## puzzle 2 
![[Pasted image 20240127034557.png]]

`&y` is a reference variable, it is an alias for the deference of x. it is also not a ptr 

![[Pasted image 20240127035416.png]]


- `y` is of type `int &`, when we print `&y` , it gives the address of the heap because again, it's an alias of the deference of ptr `x` , and `x` points to the int heap. 
- `y` itself is just 4
- bc `y` is not a pointer, can't be deferenced. 

## puzzle 3 
![[Pasted image 20240127040842.png]]
`p`,`q` are 2 int ptrs, allocated on the stacks
`p` is assigned to an int heap; 
`q` is set to also point to that heap 
![[Pasted image 20240127041500.png]]
first print `*p` should be 8
second `*p` still 8, `*q` is 9
![[Pasted image 20240127041914.png]]

## puzzle 4
![[Pasted image 20240127042246.png]]