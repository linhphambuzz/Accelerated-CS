To build our own classes 

## Templated Functions 


```
template <typename T>
class List{
	... 
	private:
	T:data; 
}; 
```

- `data` is defined as type `T`
```
template <typename T>
int max(T a, T b){
	if (a> b) {return a; }
	return b;
}
```
- both `a`  and `b` is defined with type `T`

## Compile-Time Binding

Templated variables are checked at compile time, errors are caught before running the program .

- From the `max` function above: 
```
max (4,7) //OK 
```

- Another example: 
```
max(Cube(3), Cube(6))  //Error
``` 

- Since no overloaded function for comparision is defined for `Cube` class, it will return an error