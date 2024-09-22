An anonymous method can also be assigned to an `Action` delegate:
```C#
static void Main(string[] args) {
	Action<int> printActionDel = delegate(int i) {
									Console.WriteLine(i);
								}
	printActionDel(10);     // Output: 10
}
```