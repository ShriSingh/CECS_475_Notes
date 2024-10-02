#Week3 
- Written as `Task` and `Task<result>`
- The return type is one of the following types:
	- Task --> Has a return statement -> Operand has type `<TResult`
	- Task --> Has no return statement / Has return statement with no operand
- Represents an asynchronous operation that can be awaited using the `await` keyword
- Provides several methods to create and manipulate tasks
	- Like `Task.Run`, `Task.FromResult`, and `Task.WhenAll` etc.
		- `Task.Run`
			- Method that allows us to start a task on a separate thread from the `ThreadPool`
			- Makes applications more performant and responsive
		- `Task.WhenAll`
			- Awaits the completion of all tasks in given collection
			- Returns a single task containing the results of each completed task
			- Useful for 
				- Performing multiple asynchronous operations concurrently
				- Processing their results when all are completed
		- `Task.WhenAny`
			- Awaits the completion of any tasks in a given collection
			- Returns the first completed task
			- Useful when you have multiple tasks that perform similar operations
				- You only need the result of the first one to complete
Example of `Task.Run`:
```C#
Task.Run(() =>
	{
		Console.WriteLine("Running in a separate thread!");	
	})
```
- Code snippet runs a lambda expression on a separate thread
	- Leaves the main thread free to continue executing other tasks

Another Example:
```C#
int[] numbers = Enumerable.Range(0, 1000000).ToArray();  
// Use Task.Run to start a task that computes the sum of numbers  
Task<long> task = Task.Run(() => 
	{ 
		long total = 0;  
		for (int i = 0; i < numbers.Length; i++) {  
			total += numbers[i];  
		}  
		return total;  
	});
	  
Console.WriteLine("Doing some other work...");
// Await the task to retrieve the result  
long result = await task;  
Console.WriteLine($"Sum is {result}");
```
- Using `Task.Run` offload the work to a separate thread of adding up the array of a million numbers
	- This way the main thread is free for other operations