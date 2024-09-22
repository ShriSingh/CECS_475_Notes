- A getter and/or setter that simply reads and writes to a private field of the same type as the property
- An *automatic property* declaration instructs the compiler to provide this implementation
```C#
public class Stock {
	....
	public decimal CurrentPrice { 
		get;
		set;
	}
}
```
- The compiler automatically generates a private backing field of a compiler-generated name
	- Cannot be referred to
- The `set` accessor can be marked `private` or `protected`
	- If you want to expose the property as *read-only* to other types