Anonymous Method
- A method without a name
- Can be defined using the `delegate` keyword
- Can be assigned to a variable of delegate type

Example:
```C#
public delegate void Print(int value);

static void Main(string[] args) {
	Print print = delegate(int val) {
		Console.WriteLine("Inside Anonymous method. Value {0}", val);
	};

	Print(100);      // Output: Anonymous method. Value: 100
}
```

Anonymous methods can access variable defined in an outer function.

Example:
```C#
public delegate void Print(int value);

static void Main(string[] args) {
	int i = 10;
	
	Print print = delegate(int val) {
		val += i;
		Console.WriteLine("Anonymous method: {0}", val);
	};

	print(100);         // Output: Anonymous method: 100
}
```

