A parameter is optional if
- It specifies a *default value* in its declaration
	- ```void Foo(int x = 23) { Console.WriteLine(x); }```
- Optional parameters may be omitted when calling the method
	- ```Foo();        // 23```
	- The *default argument* of 23 is passed to the optional parameter *x*
- Optional parameters can't be marked with `ref` nor `out`

[[Named Arguments]]