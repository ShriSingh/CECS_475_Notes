You can assign an anonymous method of the `Func` delegate by using the `delegate` keyword
Example:
```C#
Func<int> getRandomNumber = delegate() 
							{  
								Random rnd = new Random();  
								return rnd.Next(1, 100);  
							};
```

- **Doesn't allow `ref` and `out` parameters**