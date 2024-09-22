Trying to assign a null value to the value type variables results in a compile-time error
- Nullable types are the solution
	- Template:
		- `Nullable<T> variable_name`
		- `T? variable_name;`

Checking Nullable Type has value
- You can check if the instance of nullable type has a value
	- Using HasValue property
- Example:
```
using System;

namespace TutlaneExamples {
	class Program {
		static void Main(string[] args) {
			Nullable<int> x = null;
			
			if (x.HasValue) {
				// Access nullable type value
				Console.WriteLine("x = {0}", x.Value);
			} else {
				Console.WriteLine("Value is Empty");
			}
			
			Console.ReadLine();
		}
	}
}
```

Assigning Nullable Type to Non-Nullable Type
- Use a null-coalescing operator `??` to specify the value to be assigned
```
using System;

namespace TutlaneExamples {
	class Program {
		static void Main(string[] args) {
			int? x = null;

			// y = x if x is not null, y = 0 if x is null
			int y = x ?? 0;
			Console.WriteLine("y = {0}", y);
			Console.ReadLine();
		}
	}
}
```
