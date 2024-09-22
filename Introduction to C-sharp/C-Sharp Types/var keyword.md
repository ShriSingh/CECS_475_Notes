- Declares the implicitly typed variables 
	- *Without specifying an explicit type*
	- Example:
		- `var x = 50;     // Implicitly typed`
- The type of local variables is determined by the compiler
	- Based on the assigned value

The use of `var` optional, but while working with anonymous types, we need to declare the variables with `var`
- Need to ensure the `var` variable is declared and initialized in the same statement
- Cannot 
	- be initialized with a **null** value
	- be used as method parameters
- Don't initialized multiple implicitly-typed variables in the same statement