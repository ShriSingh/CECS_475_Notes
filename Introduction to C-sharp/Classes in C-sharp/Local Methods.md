Since C# 7, you can define a method inside another method

Example:
```C#
void WriteCubes() {
	Console.WriteLine(Cube(3));
	Console.WriteLine(Cube(4));
	Console.WriteLine(Cube(5));

	int Cube(int value) => value * value * value; // <-- this one
}
```
- Local method(`Cube`, in this case) is visible only to the enclosing(`WriteCubes`)
- Benefit of local methods
	- They can access the local variables and parameters of the enclosing method

[[Instance Constructors]]

[[Overloading Constructors]]

[[Implicit Parameterless Constructors]]

[[Constructor and Field Initialization Order]]

[[Deconstructors]]





