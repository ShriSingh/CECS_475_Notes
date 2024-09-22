A method can have a parameter of the delegate type
```C#
MyDelegate(string msg);                           // declaring a delegate  
class Program {  
	static void Main(string[] args) {  
		MyDelegate del = ClassA.MethodA;  
		InvokeDelegate(del);  
		
		del = ClassB.MethodB;  
		InvokeDelegate(del);  
		
		del = (string msg) => Console.WriteLine("Called lambda  
		expression: " + msg);  
		InvokeDelegate(del);
	}

	static void InvokeDelegate(MyDelegate del) {  // MyDelegate type parameter
		del("Hello World!");
	}
}

class ClassA {  
	static void MethodA(string message) {  
		Console.WriteLine("Called ClassA.MethodA() with parameter: " + message);  
	}  
}

class ClassB {  
	static void MethodB(string message) {  
		Console.WriteLine("Called ClassB.MethodB() with parameter: " + message);
	}  
}
```

**Note:** In .NET, `Func` and `Action` types are built-in generic delegates that should be used for most common delegates instead of creating new customer delegates.

[[Multicast Delegates]]

[[Generic Delegate]]

[[Delegate and Anonymous Method]]


