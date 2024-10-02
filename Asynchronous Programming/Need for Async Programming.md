#Week3 
Modern application often handle multiple tasks simultaneously
- Fetching data from the internet
	- Fetching data from an API
		- Making multiple API calls concurrently
```C#
public async Task<IEnumerable<string>> FetchMultipleDataAsync(IEnumerable<string> urls) { 
	// Create a new instance of HttpClient  
	using (var httpClient = new HttpClient()) { 
		// Initiate multiple GetStringAsync tasks concurrently  
		var tasks = urls.Select(url => httpClient.GetStringAsync(url));  
		// Await the completion of all tasks using Task.WhenAll  
		string[] results = await Task.WhenAll(tasks);  
		// Return the fetched data as an IEnumerable<string>
		return results;
	}
}
```
- Processing files
	- Reading or writing files
		- Reading a file asynchronously
```C#
public async Task<string> ReadFileAsync(string filePath) { 
	// Create a new instance of StreamReader with the specified file path  
	using (var reader = new StreamReader(filePath)) { 
		// Use the await keyword to read the file content asynchronously  
		string content = await reader.ReadToEndAsync();  
		// Return the content of the file when the read operation is completed  
		return content;
	}
}
```
- Performing complex calculations etc.
	- Performing CPU-bound operations (asynchronously)
```C#
public async Task<int> CalculateResultAsync(int input) { 
	// Offload the CPU-bound operation to a separate thread using Task.Run  
	int result = await Task.Run(() => PerformComplexCalculation(input));  
	// Return the result when the calculation is completed  
	return result;  
}

private int PerformComplexCalculation(int input) { 
	// Implement your complex calculation logic here  
	return input * 2;
}
```
