To write an indexer
- Define a property called `this`
	- Specifies the arguments in square brackets
For instance:
```C#
class Sentence {
	string[] words = "The quick brown fox".Split();
	
	public string this [int wordNum] {             // Indexer
		get {
			return words[wordNum];
		}

		set {
			words[wordNum] = value;
		}
	}
}
```

Here's how we could use this indexer:
```C#
Sentence s = new Sentence();
Console.WriteLine(s[3]);             // fox
s[3] = "kangaroo";
Console.WriteLine(s[3]);             // kangaroo
```

If you omit the `set` accessor, an indexer becomes *read-only* and expression-bodied syntax may be used to shorten its definition:
`public string this[int wordNum] => words[wordNum];`

