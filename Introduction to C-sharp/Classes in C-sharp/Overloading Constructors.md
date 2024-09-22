A class or struct may overload constructors.
- To avoid code duplication, one constructor may call another, using this `this` keyword:
```C#
using System;

public class Wine {
	public decimal Price;
	public int Year;
	
	public Wine(decimal price) {
		Price = price;
	}
	
	public Wine(deicmal price, int year): this (price) { // <-- This one
		Year = year;
	}
}
```

When one constructor calls another, the *called constructor* executes first.

You can pass an *expression* into another constructor as follows:
```C#
public Wine(decimal price, DateTime year): this(price, year.Year) {...}
```

