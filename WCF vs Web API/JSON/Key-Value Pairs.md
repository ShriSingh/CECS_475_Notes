#CECS475 
#Week7 
Pairs in JSON that are used to represent a property of the Object
```JSON
"FirstName" : "Virender"
     ^            ^
    Key         Value
```
- Pairs are separated by a `:` (colon)
- Key is always present in ***Double Quotes `" "`***
- Value could be anything depending on the data type
	- Could be:
		- Boolean
			- True or False
		- Number
			- Numerical values
		- Object
			- An associate array of Key-Value pairs
		- [[Array]]
			- Associate array of values
```JSON
{  
	"Description": "Map containing Country, Capital, Currency, and some States of  that Country",  
	"Region": "Asia",  
	"Countries": [  
		{  
			"Country": "India",  
			"Data": {  
				"Capital": "New Delhi",  
				"minimum temp (Degree Celsius)": 6,  
				"maximum temp (Degree Celsius)": 45,  
				"Currency": "Rupee"  
			}  
		},  
		{  
			"Country": "Nepal",  
			"Data": {  
				"Capital": "Katmandu",  
				"minimum temp (Degree Celsius)": 9,  
				"maximum temp (Degree Celsius)": 23,  
				"Currency": "Nepalese rupee"  
			}  
		}
	]
}
```