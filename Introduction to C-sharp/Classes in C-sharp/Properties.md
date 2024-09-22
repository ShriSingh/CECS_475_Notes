Properties look like fields from the outside
- But contain logic, like methods do
```C#
Stock msft = new Stock();
msft.CurrentPrice = 30;
msft.CurrentPrice -= 3;
Console.WriteLine(msft.CurrentPrice);
```
- Declared like a field, but with a `get/set` block added
```C#
public class Stock {
	decimal currentPrice;                 // The private "backing" field
	public decimal CurrentPrice {         // The public property
		get {
			return currentPrice;
		}
		
		set {
			currentPrice = value;
		}
	}      
}
```
- `get` and `set` denote property accessors
	- `get` accessor
		- Runs when the property is dead
		- Must return a value of the property's type
	- `set` accessor
		- Runs when the property is assigned

[[get and set Accessibility]]

Properties allow following modifiers:

| Modifier Type            | Modifier                                       |
| ------------------------ | ---------------------------------------------- |
| Static Modifier          | `static`                                       |
| Access Modifiers         | `public` `internal` `private` `protected`      |
| Inheritance Modifiers    | `new` `virtual` `abstract` `override` `sealed` |
| Unmanaged Code Modifiers | `unsafe` `extern`                              |

[[Read-only Calculated Properties]]

[[Property Initializers]]

[[Automatic Properties]]

[[Indexers]]


