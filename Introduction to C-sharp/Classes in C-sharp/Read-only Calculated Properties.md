- A property is read-only if
	- Specifies only a `get` accessor, and it is write-only if it specifies only a `set` accessor
- Write-only properties are rarely used
- A property typically has a dedicated backing field to store the underlying data
- A property can also be computed from other data
```c#
decimal currentPrice, sharesOwned;
```

