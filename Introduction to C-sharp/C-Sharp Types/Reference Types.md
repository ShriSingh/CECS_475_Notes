Comprises of:
- ***Class*** types
- ***Array*** types
- ***Delegate*** types
- ***Interface*** types
	- Includes pre-defined ***string*** types

A reference type is more complex than a value type
- Has two parts:
	- Object
	- Reference to that object
- The content of a reference-type variable or constant
	- is a reference to an object that contains the value
		- Allows multiple variables to refer to the same object
- Example:
	- `public class Point { public int X, Y; }`

```C#
static void Main() {
	Point p1 = new Point();
	p1.X = 7;
	
	Point p2 = p1; // Copies p1 reference
	Console.Writeline(p1.X);
	Console.WriteLine(p2.X);
	
	p1.X = 9; // Change p1.X
	
	Console.WriteLine(p1.X);
	Console.WriteLine(p2.X);
}
```

Null
- A reference can be assigned that literal `null`
	- Indicates that reference points to no object
```C#
class Point {...}

Point p = null;
Console.WriteLine(p == null); // True
	
// Following line generates a runtime error
// (a NullReferenceException is thrown):
Console.WriteLine(p.X);
```
```C#
sturct Point {...}

Point p = null; // Compile-time error
int x = null; // Compile-time error
```

| Type                       | Default Value |
| -------------------------- | ------------- |
| All reference types        | `null`        |
| All numeric and enum types | `0`           |
| `char` type                | `'\0'`        |
| `bool` type                | `false`       |
Default Values
- All type instances have a default value
- Default value for the predefined type is the result of a bitwise zeroing of memory
- You can obtain the default value for any type with the default
	- Example: `decimal d = default (decimal);`








