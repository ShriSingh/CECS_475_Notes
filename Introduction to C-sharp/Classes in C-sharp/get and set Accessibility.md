- The `get` and `set` accessors can have difference access levels
- The typical use case for this is to have a `public` property
	- With an `internal` or `private` access modifier on the setter
```C#
public class Foo {
	private decimal x;
	public decimal x {
		get {
			return x;
		}

		private set {
			x = Math.Round(value, 2);
		}
	}
}
```

