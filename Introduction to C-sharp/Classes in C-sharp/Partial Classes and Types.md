Partial Classes
- Portions of a class that the compiler can combine to form a complete class
- Can define two or more partial classes within the same file
	- General purpose of a partial class is to allow the splitting of a class definition across multiple files

```C#
// PaymentFormGen.cs - auto-generated
partial class PaymentForm { ... }

// PaymentForm.cs - hand-authored
partial class PaymentForm { ... }
```

Partial Types
- Resolved entirely by the compiler
	- Each participant must be available at compile time
	- Must reside in the same assembly
- May contain [[Partial Methods]]