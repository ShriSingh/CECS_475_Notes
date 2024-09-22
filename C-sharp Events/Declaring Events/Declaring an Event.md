Event can be declared in two steps:
- Declare a delegate
- Declare a variable of the delegate with `event` keyword
Example:
```C#
public delegate void Notify();                       // Delegate

public class ProcessBusinessLogic {
		public event Notify ProcessCompleted;        // Event 
}
```
- The `Notify` delegate specifies the signature for the `ProcessCompleted` event handler
	- It specifies that the event handler method in subscriber class must have a `void` return type and no parameters