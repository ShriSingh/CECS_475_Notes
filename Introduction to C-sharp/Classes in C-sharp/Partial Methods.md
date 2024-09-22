These let an auto-generated partial type provide hooks for manual authoring
- Examples:
```C#
partial class PaymentForm {            // In auto-generated file
	...
	partial void ValidatePayment(decimal amount);
}

partial class PaymentForm {            // In hand-authored file
	...
	partial void ValidatePayment(decimal amount) {
		if (amount > 100) {
			...
		}
	}
}
```

Consists of two parts:
- Definition
	- Typically written by a code generator
- Implementation
	- Typically manually authored
		- If not provided, the definition of the partial method is compiled away

**Note:** Partial methods must be `void` and are implicitly `private`