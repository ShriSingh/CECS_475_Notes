- May be specified on the last parameter of a method
	- That method will be able to accept any number of arguments of a particular type
		- The parameter type must be declared as an array
Example:
```C#
class Test {
	static int Sum(params int[] ints) {
		int sum = 0;
		for (int i = 0; i < ints.Length; i++) {
			sum += ints[i];                      // Increase sum by ints[i]
		}
		return sum;
	}

	static void Main() {
		int total = Sum(1, 2, 3, 4);
		Console.WriteLine(total);                // Sum = 10
	}
}
```

You can also supply a `params` argument as an ordinary array
- 1st line in `Main` is semantically equivalent to this:
	- ```int total  = Sum(new int[] {1, 2, 3, 4});```

[[Optional Parameters]]