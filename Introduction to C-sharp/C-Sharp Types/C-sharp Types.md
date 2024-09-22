All C# Types fall into following categories:
- [[Value Types]]
- [[Reference Types]]
- [[Generic Type Parameters]]
- [[Pointer Types]]

Value Types vs Reference Types
- They're handled different in memory\
- Value Types
	- Can't allow variables to refer to the same object
	- Can't have a null value
```C#
public struct Point { public int X, Y; }

Point[] a = new Point[1000];
int x = a[500].X;     // 0

public class Point { public int X, Y; }

...
Point[] a = new Point[1000];
int x = a[500].X;     // Runtime error, NullReferenceException
```
To avoid this error, we must explicitly instantiate 1,000 Points after instantiating the array.
```C#
Point[] a = new Point[1000];
for (int i = 0; i < a.Length; i++) {     // Iterate 'i' from 0 to 999
	a[i] = new Point();     // Set array element 'i' with new point 
}
```

Array
- An array *itself* is always a reference type object, regardless of the element type.
	- Following is legal:
		- `int[] a = null;`



