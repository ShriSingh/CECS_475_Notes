Essence
- Allow us to be flexible when dealing with class hierarchy

Example of class hierarchy:
```C#
public class Small {};
public class Big: Small {};
public class Bigger: Big {};
```
- `small` is base class for `big` -> `big` is a base class for `bigger`

**Note:** A derived class *will always* have something more than a base class
- Base class is relatively smaller than the derived class
```C#
Small smlC1s1 = new Small();          // Good
Small smlC1s2 = new Big();            // Good
Small smlC1s3 = new Bigger();         // Good
Big bigC1s1 = new Bigger();           // Good
Big bigC1s2 = new Small();            // BAD
```
As you can see from above,
- A base class can hold a derived class
	- But ***not the other way around***

[[Covariance in C-sharp]]

[[Contravariance in C-sharp]]

You can also use covariance and contravariance in the same method as shown below:
```c#
delegate Small covarDel(Big mc);

class Program {
	static Big Method(Small sml) {
		Console.WriteLine("Method3");

		return new Big();
	}

	static void Main(string[] args) {
		covarDel del = Method4;

		Small sm = del(new Big());
	}
}

// Output:
// Method3
```

