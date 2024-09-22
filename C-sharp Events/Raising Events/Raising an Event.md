```C#
public delegate void Notify();                  // delegate

public class ProcessBusinessLogic {
	public event Notify ProcessCompleted;       // event

	public void StartProcess() {
		Console.WriteLine("Process Started!");
		// some code here...
		OnProcessCompleted();
	}

	protected virtual void OnProcessCompleted() {    // protected virtual method
		// if ProcessCompleted is not null then call delegate
		ProcessCompleted?.Invoke();
	}
}
```
- `StartProcess()` method --> Calls --> `onProcessCompleted()` --> Raises an event
	- To raise an event, `protected` and `virtual` methods should be defined with the name `On<EventName>`
		- Protected and virtual enable derived classes to override the logic for raising the event
	- The subscriber class must register to `ProcessCompleted` event and handle it with the method whose signature matches `Notify` delegate