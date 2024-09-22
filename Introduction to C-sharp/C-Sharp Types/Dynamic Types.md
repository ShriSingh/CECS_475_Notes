Introduced to bypass the type checking at compile-time
- Resolves the type at runtime
- Same as implicitly typed local variable `var`
	- Difference being the type checking happens at runtime

Dynamic Type as a Method Parameter
- Will accept any type of parameter at run time

Assigning Class Object to Dynamic Type
- The class object properties and methods will be exposed only at runtime
- Compiler will not throw an exception when trying to access the methods or properties which don't exist in the class
