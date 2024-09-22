- You can declare variables on the fly when calling methods with `out` parameters
	- We can shorten the `Main` method
```C#
static void Main() {
	Split("Stevie Ray Vaughan", out string a, out string b);
	Console.WriteLine(a);               // Stevie ray
	Console.WriteLine(b);               // Vaughan
}
```
- You can "discard" uninterested/unused `out` parameters
	- Compiler treats the underscore as a special symbol
```C#
Split("Steve Ray Vaughan", out string a, out _); // Discard the 2nd param
Console.WriteLine(a);
```