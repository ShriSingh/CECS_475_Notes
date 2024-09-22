Similar to a `Func` delegate, but ***doesn't return a value***
- Can ***only*** be used with a method that has a `void` return type
Example:
```C#
static void ConsolePrint(int i) {
	Console.WriteLine(i);
}

static void Main(string[] args) {
	Action<int> printActionDel = ConsolePrint;
	printActionDel(10);     // Output: 10
}
```

- Can initialize an `Action` delegate using the `new` keyword or directly assigning a method:
```C#
Action<int> printActionDel = ConsolePrint;
// Or
Action<int> printActionDel = new Action<int>(ConsolePrint);
```

- Can take up to 16 input parameters of different types

[[Action with an Anonymous Method]]

[[Action with Lambda Expression]]