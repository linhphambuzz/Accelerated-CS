## Definition 

- Heap memory allows us to create memory that is completely independent of a life cycle of a function, unlike stacked memory.
-  **Heap memory starts low and goes up** 
## New operator 
1. is an operator in C++ that's going to return a pointer to the memory address starting of the new data, and not an instance of the data itself.
2.  Do 3 things: 
	- allocate memory on the heap for a data structure, whatever the data structure is that we're allocating
	- It's going to initialize that data structure
	- And it's going to return a pointer to start off that data structure
3. it doesn't matter if we return from the function, doesn't matter if the function ends, the only time the system ever gets back this memory is when we use the delete keyword
4. Example: 
```
int *numPtr= new int; 
```
	From the example above: 
		- lhs: stack memory allocated 
		- rhs: new heap memory 
		- 

![[heap.png]]
5. Another example 

```
int main() {

int *numPtr = new int;



std::cout << "*numPtr: " << *numPtr << std::endl;

std::cout << " numPtr: " << numPtr << std::endl;

std::cout << "&numPtr: " << &numPtr << std::endl;

  

*numPtr = 42;

std::cout << "*numPtr assigned 42." << std::endl;

  

std::cout << "*numPtr: " << *numPtr << std::endl;

std::cout << " numPtr: " << numPtr << std::endl;

std::cout << "&numPtr: " << &numPtr << std::endl;

  

return 0;

}
```

- ` *numPtr`: is the deference of `numPtr` . It will show what's it pointing to in the heap, random int could be printed out , expect small number
- `numPtr` itself is an int pointer, content will be address of heap memory 
- `&numPtr` is the address of `numPtr` in the stack, expect large number

Now, after `*numPtr = 42`: 
- `*numPtr`  is changed to 42, this is what contained in the heap memory
- `numPtr` is not changed, because the heap memory it points to is fix 
- `&numPtr` stack memory isn't changed either

Here's the outcome of the code above: 
![[heap2.png]]


## Null pointer

```
int *p = new int;

Cube *c = new Cube;

*p = 42;

(*c).setLength(4);
```

Before the delete: 
![[heap3.png]]


```
delete c;

delete p;
```
After the delete: 
![[heap4.png.png]]


`int* p ` and `cube *c` is pointing to nothing, to solve this: NULL pointer

- ptr to nowhere
- 0x0 is reserved, never be used by the system 
-  0x0 will generate segmented fault when accessed 
- call to delete is ignored 
```
delete c; c = nullptr;

delete p; p = nullptr
```

## arrow operator 
-  when the object is stored via pointer, we can access the number functions using the arrow operator 
- `(*c).setLength(4);` is equal to  `c->setLength(4)`
- this is: we're going to directly deference value of c (which is a ptr of type `Cube` ), then we get to the member function of `Cube`
- example:  
Before the delete: 

![[heap5.png]]

`c1` is pointing to the lowest heap for memory of Cube, `c2` is set to point to what `c1` is pointing to. 
`c2->setLenth(10)` set the length of object to 10 . 


when `delete c2;` :

![[Pasted image 20240127030353.png]]
The heap contains nothing. 
Now when we delete `c1`, nothing is to be deleted.. return error!!! 