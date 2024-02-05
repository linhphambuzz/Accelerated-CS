
``
```
unsigned int b = 8;
```
- can't handle negative values 
```
std::cout << (x-y) << std::endl; \\throw large number
```

- to make it useable, cast back to int: 
```
std::cout << (int)(x-y) << std::endl;

```

- or assign back to an int var: 
```
int z = x - y;

std::cout << z << std::endl;
```