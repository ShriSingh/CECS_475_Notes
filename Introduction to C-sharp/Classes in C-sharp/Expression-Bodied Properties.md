Example:
```C#
public decimal Worth {
	get => currentPrice * sharesOwned;
	set => sharesOwned = value / currentPrice;
}
```
