#Week3 
- Can **only** be used within an `async` method
- Can be applied to any expression that returns a `Task` or `Task<result>` object
- Unwraps the result of the `Task<TResult>` object
	- Allowing you to catch and handle them in the calling async method
- Can be used with `using`, `foreach`, and `lock` statements in C# 8.0 & later