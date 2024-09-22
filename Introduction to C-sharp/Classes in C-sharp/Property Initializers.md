You can add a property initializer to automatic properties
- Just as fields
	- `public decimal CurrentPrice { get; set; } = 123;`
		- Gives `CurrentPrice` an initial value of 123
- Properties with an initializer can be read-only
	- `public int Maximum { get; } = 999;`