1. if-else 

```

if (condition1) {

}

else if (condition2) {

}

else if (condition3) {

}

else {

	// If none of the other conditions were met...

}
```

2. if-else one-line 
```
// Since (5<10) is true, the expression before the colon will be selected, which is 1.

int x = 5 < 10 ? 1 : 2;

// Now x is equal to 1.

// Note, the following syntax is NOT allowed in C++, which is why the ternary operator can be useful in these cases:

int y = if (5<10) {1;} else {2;}
```


3. Type-casting
```
#include <iostream>

int main() {

int x = 2;

double y = 3.5;

std::cout << "This result will be a double with value 5.5: " << (x+y) << std::endl;

int z = x+y; // This expression is calculated as a double, but then it's cast back to int!

std::cout << "This result will be an int with value 5: " << z << std::endl;

return 0;

}
```

3. Boolean 
- In C++, non-zero value is considered `True`, 0 is `False`
