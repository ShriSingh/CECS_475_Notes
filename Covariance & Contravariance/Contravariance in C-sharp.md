Is applied to **parameters**
- Allows a method with the parameter of a base class to be assigned to a delegate the expects the parameter of a derived class
Example:
```C#
public delegate Small covarDel(Big mc);  

class Program {  
	static Big Method1(Big bg) {  
		Console.WriteLine("Method1");  
		return new Big();
	}  

	static Small Method2(Big bg) {  
		Console.WriteLine("Method2");  
		return new Small();
	}  
	
	static Small Method3(Small sml) {  
		Console.WriteLine("Method3");  
		return new Small();
	}

	static void Main(string[] args) {  
		covarDel del = Method1;  
		del += Method2;  
		del += Method3;  
		
		Small sm = del(new Big());
	}
}

// Output:
// Method1
// Method2
// Method3
```
- As you can see, `Method3` has a parameter of Small class whereas delegate expects a parameter of `Big` class. Still, you can use `Method3` with the delegate


