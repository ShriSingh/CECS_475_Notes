Both are a part of the signature
- `Foo(int)` can coexist with `Foo(ref int)` *or*  `Foo(out int)`
	- `Foo(out int)` **and** `Foo(out int)` **cannot coexist**
Example:
```C#
void Foo(int x) {...}
void Foo(ref int x) {...}        // Ok so far
void Foo(out int x) {...}        // Compile-time error
```