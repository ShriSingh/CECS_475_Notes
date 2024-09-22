If you want to pass more than one value as event data, then create a class deriving from the `EventArgs` base class, as shown below:
```C#
public void StartProcess() {  
	try {  
		Console.WriteLine("Process Started!");  
		// some code here..  
		OnProcessCompleted(true);  
	} catch(Exception ex) {  
		OnProcessCompleted(false);
	}  
}  

	protected virtual void OnProcessCompleted(bool IsSuccessful) {  
		ProcessCompleted?.Invoke(this, IsSuccessful);  
	}  
}

class ProcessEventArgs : EventArgs {  
	public bool IsSuccessful { get; set; }  
	public DateTime CompletionTime { get; set; }  
}
```

The following example shows how to pass custom `ProcessEventArgs` class to the handler.
Example:
```C#
class Program {  
	public static void Main() {  
		ProcessBusinessLogic bl = new ProcessBusinessLogic();  
		bl.ProcessCompleted += bl_ProcessCompleted; // register with an event  
		bl.StartProcess();
	}  
	
	// event handler  
	public static void bl_ProcessCompleted(object sender, ProcessEventArgs e) {  
		Console.WriteLine("Process " + (e.IsSuccessful? "Completed Successfully": "failed"));  
		Console.WriteLine("Completion Time: " + e.CompletionTime.ToLongDateString());  
	}  
}

public class ProcessBusinessLogic {  
	// declaring an event using built-in EventHandler  
	public event EventHandler<ProcessEventArgs> ProcessCompleted;
	
	public void StartProcess() {
		var data = new ProcessEventArgs();
		
		try {  
			Console.WriteLine("Process Started!");
			  
			// some code here..  
			
			data.IsSuccessful = true;  
			data.CompletionTime = DateTime.Now;  
			OnProcessCompleted(data);  
		} catch(Exception ex) {  
			data.IsSuccessful = false;  
			data.CompletionTime = DateTime.Now;  
			OnProcessCompleted(data);  
		}  
	}  

	protected virtual void OnProcessCompleted(ProcessEventArgs e) {  
		ProcessCompleted?.Invoke(this, e);  
	}  
}
```