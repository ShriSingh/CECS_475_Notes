Can be defined the same way as a delegate
- You have to use generic type parameters or return type
	- Must be specified when you set a target method

Example:
```C#
public delegate T add<T>(T param1, T param2);     // Generic delegate

class Program {  
	static void Main(string[] args) {  
		add<int> sum = Sum;  
		Console.WriteLine(sum(10, 20));  
		
		add<string> con = Concat;  
		Console.WriteLine(conct("Hello ","World!!"));  
	}  
	
	public static int Sum(int val1, int val2) {  
		return val1 + val2;  
	}
	
	public static string Concat(string str1, string str2) {  
		return str1 + str2;
	}  
}
```

[[Generic Delegate Types]]
