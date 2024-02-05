 Constructor
 1. Automatic default constructor
	 - Initialize all of the member variables to their default values

2. Custom default constructor 
	- member function that has the same name as the class itself.
	- no parameter taken
	- no return 

```

class Cube {

public:

	Cube(); // Custom default constructor

	double getVolume();

	double getSurfaceArea();

	void setLength(double length);

```


In main: 

```

int main() {

uiuc::Cube c;

std::cout << "Volume: " << c.getVolume() << std::endl;

return 0;

}
```

3. Custom constructor 
	- take in parameters 

```
class Cube {

public:

Cube(); // Custom default constructor

Cube(double length); // One argument constructor

  

double getVolume();

double getSurfaceArea();

void setLength(double length);

  

private:

double length_;

};
```

In main: 

```
int main() {

uiuc::Cube c(2);

std::cout << "Volume: " << c.getVolume() << std::endl;

return 0;

}
```
