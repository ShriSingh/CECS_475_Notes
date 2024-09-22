- A variable that is a member of a class or struct\
	- Of any type
Example:
```C#
class Octopus {
	string name;                // string variable
	public int Age = 10;        // int variable 
}
```

| Modifer Type         | Example                             |
| -------------------- | ----------------------------------- |
| Static modifier      | `static`                            |
| Access modifiers     | `public internal private protected` |
| Inheritance modifier | `new`                               |
| Unsafe code modifier | `unsafe`                            |
| Read-only modifier   | `readonly`                          |
| Threading modifier   | `volatile`                          |
`readonly` Modifier
- Prevents a field from being modified after construction
- Can be assigned only in its declaration
	- Or within the enclosing type's constructor

Field Initialization
- Optional
	- Default value of an uninitialized field
		- `(0, \0, null, false)`
- Run before constructors

[[Field vs Property]]





