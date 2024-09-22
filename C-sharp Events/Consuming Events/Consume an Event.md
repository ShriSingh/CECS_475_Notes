```C#
class Program {
	public static void Main() {
		ProcessBusinessLogic bl = new ProcessBusinessLogic();
		bl.ProcessCompleted += bl_ProcessCompleted;    // Register with an event
		bl.StartProcess();
	}

	// Event handler
	public static void bl_ProcessCompleted() {
		Console.WriteLine("Process Completed!");
	}
}
```


