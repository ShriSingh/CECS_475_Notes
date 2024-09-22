```C#
Func<int> getRandomNumber = () => new Random().Next(1, 100);  
// Or  
Func<int, int, int> Sum = (x, y) => x + y;
```