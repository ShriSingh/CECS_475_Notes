The following pairs of methods cannot coexist in the same type
- Return type and the `params` modifier are not part of a method's signature
```C#
void Foo(int x) {...}
float Foo(int x) {...}           // Compile-time error

void Foo(int[] x) {...}
void Foo(params int[] x) {...}   // Compile-time error
```

