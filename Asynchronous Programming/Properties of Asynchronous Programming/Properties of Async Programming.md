#Week3 
Asynchronous programming is done using:
- Language features like
	- [[async]]/[[await]] keywords
		- Designed to make it easier to write asynchronous code
			- Can run in the background while other code is executing
		- Using both elements allow developers to:
			- Create highly performant applications which are able to process multiple requests simultaneously
				- Without waiting on any particular task or operation to complete before continuing with other work items in its queue\
	- [[Task or Task(result)]]
- Example:
```C#
using System.Threading;
using System.Threading.Tasks;

namespace ConsoleAppl {
	internal class Program {
		public async static Task Main(string[] args) {
			Console.WriteLine("Start of the program.");
			// Asynchronous method call with Task-based pattern
			Task<string> dataTask = GetExternalDataAsync();
			// Do other tasks while waiting for the data
			Console.WriteLine("Doing some other task by printing this line.")

			for (int i = 0; i < 5; i++) {
				Console.WriteLine(i);
			}
			
			// Waiting for the data to complete and get the result
			string data = await dataTask;
			Console.WriteLine("Data : " + data);
			Console.WriteLine("End of the program.");
		}

		public static async Task<string> GetExternalDataAsync() {
			await Task.Delay(5000);  // Simulating an asynchronous operating by delaying a 2 second
			return "Sample data from GetExternalDataAsync() method.";
		}
	}
}

// Runtime Output:
/*
Doing some other task by printing this line.
0
1
2
3
4
Data: Sample data from GetExternalDataAsync() method
*/
```

Another Example:
```C#
public async Task<string> FetchAndProcessDataAsync() { 
	// Call the FetchDataAsync method and await its completion  
	string rawData = await FetchDataAsync();  
	// Process the raw data (e.g., parsing JSON, XML, or other transformations)  
	string processedData = ProcessData(rawData);  
	// Return the processed data  
	return processedData;  
}

private string ProcessData(string rawData) { 
	// Implement your data processing logic here  
	return rawData.ToUpper();
}
```







