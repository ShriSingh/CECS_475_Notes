A type that represents a reference to a method with a specific signature.
- Provides flexibility of the application and code reuse
- Lets you decide which method to call at runtime
- You define variables of delegate
	- Like any other data type
		- They can refer to any methods **with same signature as the delegate**

3 Steps involved while working with delegates
- Declare the delegate
	- Using the `delegate` keyword, followed by a function signature
		- Delegate Syntax
			- `[access modifier] delegate [return type] [delegate name]([parameters])`
			- Example:
				- `public delegate void MyDelegate(string msg);`
	- Can be declared outside of the class or inside the class
		- Practically, it should be declared out of the class
- Set the target method
	- Or set a lambda expression
	- Done by creating an object of the delegate using the keyword and passing a method whose signature matches the delegate signature
- Invoke the delegate

```C#
public delegate void MyDelegate(string msg);       // Declare a delegate

// Set target method
MyDelegate del = new MyDelegate(MethodA);
// or
MyDelegate del = MethodA;
// or set a lambda expression
MyDelegate del = (string msg) => Console.WriteLine(msg);

// Target method
static void MethodA(string message) {
	Console.WriteLine(message);
}

// Invoke the delegate
del.Invoke("Hello World!");
// or
del("Hello World!");
```

![[delegate-mapping.webp]]
