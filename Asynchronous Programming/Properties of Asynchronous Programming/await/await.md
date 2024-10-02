#Week3 
Tells the compiler that it should wait until all operations within an `async` method have completed before continuing with subsequent instructions in the program flow.
- Used within an `async` method to temporarily suspend its execution
	- Yield control back to the calling method until the awaited task is completed
- This allows other tasks to continue executing in the meantime
	- Ensuring that the application remains responsive

[[await Properties]]


