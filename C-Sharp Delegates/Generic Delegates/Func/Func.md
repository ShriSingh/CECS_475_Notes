Generic delegate included in the `System` namespace
- It has 
	- Zero to 16 `in` parameters
		- Input parameter
	- At least one `out` parameter
		- Must return a value
Example:
```C#
namespace System {
	public delegate TResult Func<in T, out TResult>(T arg);
}
```
- The last parameter in `<>` is the considered the return type
```C#
Func<int, int, int> sum; // Input type: int, Return type: int
```

[[Func with Anonymous Method]]

[[Func with Lambda Expression]]

