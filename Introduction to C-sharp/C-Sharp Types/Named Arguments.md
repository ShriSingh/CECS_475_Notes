Identifying an argument can be done by **name**, instead of **position**
- Named arguments can occur in any order
	- Works well with optional parameters
		- Useful when calling COM APIs
	- `void Bar(int a = 0, int b = 0, int c = 0, int d = 3, ...); => Bar(d: 3);`
- Can also mix named, and positional arguments
	- **Restriction:** *Positional arguments come before named arguments*
		- `Foo(x: 1, 2); // Compile-time error`
```C#
void Foo(int x, int y) {
	Console.WriteLine(x + ", " + y);
}

void Test() {
	Foo(x: 1, y: 2);             // 1, 2
	// Semantically identical as Foo(y: 2, x: 1)
}
```

