Delegate can point to multiple methods.
- `"+"` or `"+="` operator adds a function to the invocation list
- `"-"` or `"-="` operator operator removes it

```C#
public delegate void MyDelegate(string msg); //declaring a delegate  

class Program {
	static void Main(string[] args) {  
		MyDelegate del1 = ClassA.MethodA;  
		MyDelegate del2 = ClassB.MethodB;
		  
		MyDelegate del = del1 + del2; // combines del1 + del2  
		del("Hello World");  
		
		MyDelegate del3 = (string msg) => Console.WriteLine("Called lambda expression: " + msg);
		del += del3; // combines del1 + del2 + del3  
		del("Hello World");  

		del = del - del2; // removes del2  
		del("Hello World");  
		
		del -= del1 // removes del1  
		del("Hello World");
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

**Note:** If a delegate returns a value, then the last assigned target method's value will be return when a multicast delegate called
```C#
MyDelegate del = del1 + del2;
Console.WriteLine(del());       // returns 200
```
