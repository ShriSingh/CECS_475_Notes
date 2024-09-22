Parameters
- A method has a sequence of parameters
Example:
```C#
static void Foo (int p) {
	p = p + 1;                     // Increment p by 1
	Console.WriteLine(p);          // Write p to screen 
}

static void Main() {
	Foo(8);                        // Call Foo with an argument of 8
}
```

You can control how parameters are passed with [[ref and out modifiers]]:

[[Passing Arguments by Value]]

[[Out Variables and Discards]]

[[Implications of Passing by Reference]]

[[Params Modifier]]




