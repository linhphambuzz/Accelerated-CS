## for loop 
```
int x = -1;
for (int x = 0; x <= 2; x++) {
	std::cout << "[Inside the loop] x is now: " << x << std::endl;
}
```
- x is declared in the loop, x is in the inner scope
```
for (x = 0; x <= 2; x++) {

std::cout << "[Inside the loop] x is now: " << x << std::endl;

}
std::cout << "[Outside the loop] x is now (should be 3): " << x << std::endl;
```
- `x` isn't declared as the inner scope variable. 
- this modifies the outer x directly

## while loop 
```
while (x <= 3) {

	std::cout << "x is now: " << x << std::endl;

	x++; // increment x by 1

}
```
