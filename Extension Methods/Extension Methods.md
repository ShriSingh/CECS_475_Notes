Are additional methods
- Allow you to inject additional methods
	- Without modifying, deriving, or recompiling the original class, struct, or interface
- Can be added to your 
	- own custom class
	- .NET Framework classes
	- 3rd party classes or interfaces
- A special kind of static method defined a static class
	- To define an extension method, define a static class
- Have a special symbol in intellisense
	- Helps differentiate between class and extension methods
Example:
```C#
int i = 10;
bool result = i.IsGreaterThan(100);       // Returns false
```
The `IsGreaterThan()` method above is not a method of int data type(Int32 struct)
- An extension method written by the programmer for the int data type
- The method will be available throughout the application
	- Include the `namespace` in which it has been defined
Example:
```C#
namespace ExtensionMethods {
	public static class IntExtensions {
		...
	}
}
```
Now we define a static method as an extension method
- 1st parameter of the extension method specifies the type
	- Must be preceded with `this` modifier
Like this:
```C#
namespace ExtensionMethods {
	public static class IntExtensions {
		public static bool IsGreaterThan(this int i, int value) {
			return i > value;
		}
	}
}
```

Now you can include the Extension methods `namespace` wherever you want to use this extension method
```C#
using ExtensionMethods;

class Program {
	static void Main(string[] args) {
		int i = 10;
		bool result = i.IsGreaterThan(100);
		
		Console.WriteLine(result);       // Output: false
	}
}
```

[[Benefits of Extension Methods]]

External Links:
- https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-  
structs/how-to-implement-and-call-a-custom-extension-method  
- https://www.c-sharpcorner.com/UploadFile/puranindia/extension-methods-in-C-Sharp-3-0
