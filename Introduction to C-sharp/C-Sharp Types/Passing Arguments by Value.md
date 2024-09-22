- Arguments in C# are passed by ***value***
	- Most common value
- Passing a reference-type argument by value copies the reference
	- **NOT the object**
```C#
class Test {
	static void Foo(int p) {
		p = p + 1;                     // Increment p by 1
		Console.WriteLine(p);          // Write p to screen
	}
	
	static void Main() {
		int x = 8;
		Foo(x);                        // Make a copy of 'x'
		Console.WriteLine(x);          // 'x' will still by 8
	}
}
```
