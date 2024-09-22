- Called a *deconstructor method*
	- C# 7 introduced the deconstructor pattern
- Acts as an approximate opposite to a constructor
- Are methods inside the class used to destroy instances of that class
	- When they are not needed
- Called implicitly by the .NET Framework's garbage collector
	- Programmer has no control as when to invoke the destructor
- Must be called `Deconstruct`
	- Have one or more `out` parameters

Examples:
```C#
public void Deconstruct(out float width, out float height) {
	width = Width;
	height = Height;
}
```

- To call the deconstructor, we use the following special syntax:
	- `var rect = new Rectangle(3, 4);`
```C#
(float width, float weight) = rect;            // Deconstruction
Console.WriteLine(width + " " + height);       // 3 4

// Our deconstructing call is equivalent to:
float width, height;
rect.Deonstruct(out width, out height);

Or:

rect.Deconstruct(out var width, out var height);
```

[[Deconstructors vs Constructors]]

[[Deconstructor Assignment]]
