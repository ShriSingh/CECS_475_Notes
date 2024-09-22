Most events send some data to the subscribers
- The `EventArgs` class is the base class for all the event data classes
	- .NET includes many event data classes such as `SerialDataReceivedEventArgs`
		- They follow a naming pattern of ending all event data classes with `EventArgs`
		- You can create you custom class for event data
			- By deriving `EventArgs` class
Example:
```C#
class Program {
	public static void Main() {
		ProcessBusiness Logic bl = new ProcessBusinessLogic();
		bl.ProcessCompleted += bl_ProcessCompleted;      // Register with an event
		bl.StartProcess();
	}

	// Event handler
	public static void bl_ProcessCompleted(object sender, bool IsSuccessful) {
		Console.WriteLine("Process " + (IsSuccessful? "Completed Successfully": "failed"));
	}

	public class ProcessBusinessLogic {
		// Declaring an event using built-in EventHandler
		public event EventHandler<bool> ProcessCompleted;
	}
}
```
- We're passing a single Boolean value to the handlers that indicate whether the process completed successfully or not

[[Passing Custom EventArgs]]
