Class-only methods that
- Execute before the garbage collector reclaims the memory for an unreferenced object

Syntax for a finalizer is the name of the class prefixed with the `~` symbol
```C#
class Class1 {
	~Class1() {
	...
	}
}
```

This is actually C# syntax for overriding `Object's Finalize` method
- The compiler expands it into the following method declaration
```C#
protected override void Finalize () {
	...
	base.Finalize();
}
```

[[Destructors vs Finalizers]]

