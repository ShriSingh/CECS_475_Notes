| Parameter Modifier | Passed by | Variable assigned |
| ------------------ | --------- | ----------------- |
| (None)             | Reference | *Going in*        |
| `ref`              | Reference | *Going in*        |
| `out`              | Reference | *Going out*       |

- `ref` modifier
	- Used to *pass by reference*
	- Required both when writing and calling the method
```C#
class Test {
	static void Foo(ref int p) {
		p = p + 1;                     // Increment p by 1
		Console.WriteLine(p);          // Write p to screen
	}
	
	static void Main() {
		int x = 8;
		Foo(ref x);                    // Ask Foo to deal directly with x
		Console.WriteLine(x);          // 'x' is now 9
	}
}
```
- `out` modifier
	- Like a `ref` argument(also *pass by reference*), except
		- Need not be assigned before going into the function
		- Must be assigned before it comes *out* of the function
	- Commonly used to get multiple return values back from a method
```C#
class Test {
	static void Split(string name, out string firstNames,  out string lastName) {
		int i = name.LastIndexOf(' ');
		firstNames = name.SubString(0, i);
		lastName = name.SubString(i + 1);
	}

	static void Main() {
		string a, b;
		Split("Stevie Ray Vaughan", out a, out b);
		Console.WriteLine(a);             // Stevie May
		Console.WriteLine(b);             // Vaughan
	}
}
```

[[Ref Locals]]
