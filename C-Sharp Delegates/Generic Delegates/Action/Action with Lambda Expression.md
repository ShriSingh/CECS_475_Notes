```C#
static void Main(string[] args) {
	Action<int> printActionDel = i => Console.WriteLine(i);

	printActionDel(10);
}
```
