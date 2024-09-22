A static constructor executes once per *type*
- Rather then once per *instance*
- A type can define only one static constructor
	- It must be parameterless and have the same name as the type
```C#
class Test {
	static Test() {
		Console.WriteLine("Type Initialized");
	}
}
```

The runtime automatically invokes a static constructor just prior to the type being used.
- Two things trigger this:
	- Instantiating the type
	- Accessing a static member in the type

**Note:** Only modifiers allowed by static constructors are `unsafe` and `extern`


