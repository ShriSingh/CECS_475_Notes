Lets you define a local variable that *references* an element in an array or field in an object
- Added in C# 7
```C#
int[] numbers = { 0, 1, 2, 3, 4 };
ref int numRef = ref numbers [2];     // numRef is refernce to the numbers[2]

numRef *= 10;
Console.WriteLine(numRef);            // 20
Console.WriteLine(numbers[2]);        // 20
```
- Target for a `ref` local must an array element, field, or local variable
	- Can't be a *property*
- Intended for specialized micro-optimization scenarios
	- Typically used in conjunction with *ref returns*
