Allows flexibility in the **return type of delegate methods**
- Allows to assign a method to the delegate that has a less derived return type
Example: Covariance with Delegate
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

	static void Main(string[] args) {
		covarDel del = Method1;

		Small sm1 = del(new Big());

		del = Method2;

		Small sm1 = del(new Big());
	}
}

// Output:
// Method1
// Method2
```
- Delegate expects a return type of `Small`(base class), but we can still assign `Method1` that returns `Big`(derived class) and also `Method2` that has some signature as delegate expects
- 