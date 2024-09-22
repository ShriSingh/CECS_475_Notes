You pass an argument by reference
- You alias the storage location of an existing variable than create a new storage solution

In the following example, variables `x` and `y` represent the same instance:
```C#
class Test {
	static int x;
	
	static void Main() {
		Foo(out x);	
	}

	static void Foo (out int y) {
		Console.WriteLine(x);                 // x is 0
		y = 1;                                // Mutate y
		Console.WriteLine(x);                 // x is 1
	}
}
```

