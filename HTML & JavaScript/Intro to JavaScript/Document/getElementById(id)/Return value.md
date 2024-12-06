#CECS475 #Week8 
An Element object describing the DOM element object matching the specified ID or null if no matching element was found in the document.

HTML
```HTML
<html lang="en">
	<head>
		<title>getElementById example</title>
	</head>
	<body>
		<p id="para">Some text here</p>
		<button onclick="changeColor('blue');">blue</button>
		<button onclick="changeColor('red');">red</button>
	</body>
</html>
```

JavaScript
```JavaScript
function changeColor(newColor) {
	const elem = document.getElementById("para");
	elem.style.color = newColor;
}
```

Result
```
Some text here

blue red
```