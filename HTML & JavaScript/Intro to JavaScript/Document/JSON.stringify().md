#CECS475 #Week8 
- A common use of JSON is use to exchange data to/from a web server
- When sending data to a web server, the data has to be string
- Convert a JavaScript object into a string with `JSON.stringify()`

Example:
```JavaScript
// Imagine we have this object in JavaScript:
const obj = {name: "John", age: 30, city: "New York"};
// Use the JSON.Stringify() to convert it into a string
const myJSON = JSON.stringify(obj);
```

HTML
```HTML
<!DOCTYPE html>  
<html>  
	<body>  
		<h2>Create a JSON string from a JavaScript object.</h2>  
		<p id="demo"></p>  
		<script>  
			const obj = {name: "John", age: 30, city: "New York"};  
			const myJSON = JSON.stringify(obj);  
			document.getElementById("demo").innerHTML = myJSON;  
		</script>  
	</body>  
</html>

<!--Creates a JSON string from a JavaScript object-->
<!--{"name": "John", "age": 30, "city": "New York"}-->
```