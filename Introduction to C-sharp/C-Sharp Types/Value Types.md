Comprises of:
- Most built-in types
	- All numeric types, ***char*** type, and ***bool*** type
- Custom ***struct*** and ***enum*** types

The content of a ***value*** type variable or constant is simply a value
- Examples
	- `int` = 32 bits of data
	- custom value type with `struct` keyword: `public struct Point{public int X, public int Y}`
		- The assignment of a value-type instance always copies the instance
		- `X` and `Y` are value/instance

```C#
static void Main() {  
	Point p1 = new Point();  
	p1.X = 7
	Point p2 = p1; // Assignment causes copy
	
	Console.WriteLine (p1.X); // 7  
	Console.WriteLine (p2.X); // 7
	
	p1.X = 9; // Change p1.X
	
	Console.WriteLine (p1.X); // 9;
	Console.WriteLine (p2.X); // 7;
}
```

Numeric Type:
![[Pasted image 20240903220506.png]]
- Interval Types
	-  `int` and `long` are favored by both C# and the runtime
- `real` number Types
	- `float` and `double` are *floating-point* types
		- Used for scientific and graphical calculations
	- `decimal`
		- Had base-10-accruate arithmetic and high precision
		- Used for financial calculations