Fields can be initialized with default values in their declaration
```C#
class Player {
	int shields = 50;      // Initialized first
	int health = 100;      // Initialized second
}
```

Field initializations occur *before* the constructor is executed, and in the declaration order of the fields

[[Static Constructors]]

