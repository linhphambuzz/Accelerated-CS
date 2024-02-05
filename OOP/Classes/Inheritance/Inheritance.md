-  concept in C++ that allows us to inherit all of the member functions and the data from a base class into a derived class.

```
\\ Shape is the base class 
clas Cube : public Shape {
	
	}

```

- `Cube` is inherited from `Shape`
## Initialization
- When a derived class is inititialized, thve derived class must construct the base class 
- `Cube` must construct `Shape`
- By default, uses default constructor
- Custom Constructor can be used with an initialization list. 

```
Cube::Cube(double width, uiuc::HSLAPixel color) : Shape(width) {
	color_ = color;
}
```
 
 - `Shape` is constructed before `Cube`

## Access Control 
- When a base class inherited, we can access all of the public members of the base class, but we cannot access any of the private members of the base class.

```
double Cube::getVolume() const {

// Cannot access Shape::width_ due to it being `private`

// ...instead we use the public Shape::getWidth(), a public function
return getWidth() * getWidth() * getWidth();

}
```
- Since `width_` is a private variable, we have to use `getWidth()` which is a public attribute of the `Shape` based class. 
## Initializer List
- initialize in the base class
- initialize the current class via another constructor.
- initialize default values and member variables 
```
Shape::Shape() : Shape(1) {
// Nothing.
}
```
- Initializer here init the constructor that takes 1 param (i.e `Shape(double width);` in `Shape.h`)
```
Shape::Shape(double width) : width_(width) {
// Nothing.
}
```

- The custom constructor with one param here has the initilizer list of `width_(width)` that initialize the private variable `width_` to be `width`.(i.e:1)