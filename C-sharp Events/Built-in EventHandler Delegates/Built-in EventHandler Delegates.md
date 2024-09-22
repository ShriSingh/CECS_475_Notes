- .NET Framework includes built-in delegate types for the most common events
	- `EventHandler` and  `EventHandler<TEventArgs>`
- Any event should include 2 parameters:
	- Source of the event
	- Event data

[[Which delegate to use]]

Example:
```C#
public class ProcessBusiness Logic {
	// declaring an event using built-in EventHandler
	public event EvenHandler ProcessCompleted;
}

public void StartProcess() {
	Console.WriteLine("Process Started!");
	// some code here...
	OnProcessCompleted(EventArgs.Empty);      // No event data

	protected virtual void OnProcessCompleted(EventArgs e) {
		ProcessCompleted?.Invoke(this, e);
	}
}

class Program {
	public static void Main() {
		ProcessBusinessLogic bl = new ProcessBusinessLogic();
		bl.ProcessCompleted += bl_ProcessCompleted;    // register with an event
		bl.StartProcess();
	}

	// event handler
	public static void bl_ProcessCompleted(object sender, EventArgs e) {
		Console.WriteLine("Process Completed!");
	}	
}
```
- The event handler `bl_ProcessCompleted()` method includes two parameters that match with EventHandler delegate
	- passing `this` as a sender and `EventArgs.Empty`, when we raise an event using `Invoke()` in the `OnProcessCompleted()` method

External Links:
- https://learn.microsoft.com/en-us/dotnet/api/system.eventhandler?view=net-8.0
- https://learn.microsoft.com/en-us/dotnet/api/system.eventhandler-1?view=net-8.0