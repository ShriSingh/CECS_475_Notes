#Week5 
A query language designed to be used with the Entity Framework
- Are database independent
- Looks similar to [[Native SQL]]
Example:
```C#
class QueryVMethodSyntax {
	static void Main() {
		int[] numbers = { 5, 10, 8, 3, 6, 12 }; // Query syntax;
		IEnumerable<int> numQuery1 = {
			from num in numbers
			where num % 2 == 0
			orderby num
			select num;
		} 
	}
}

// Method Syntax
IEnumerable<int> numQuery2 = numbers.Where(num => num % 2 == 0).OrderBy(n => n);

foreach (int i in numQuery1) {
	Console.Write(i + " ");
}
Console.WriteLine(System.Environment.NewLine);

foreach (int i in numQuery2) {
	Console.Write(i + " ");
}
```