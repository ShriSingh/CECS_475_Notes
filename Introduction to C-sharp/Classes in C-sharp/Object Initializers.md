To simplify object initialization:
- Any accessible fields or properties of an object can be set via an *object initializer* after construction
```C#
public class Bunny {
	public string Name;
	public bool LikesCarrots;
	public bool LikesHumans;

	public Bunny() {}
	public Bunny(string n) { Name = n; }
}

// Notr parameterless constructors can omit empty parentheses
Bunny b1 = new Bunny {Name="Bo", LikesCarrots=true, LikesHumans=false};
Bunny b2 = new Bunny("Bo") {LikesCarrots=true, LikesHumans=false};
```
