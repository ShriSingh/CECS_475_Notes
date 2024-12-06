#CECS475 #Week8 
Changing HTML Content with inner
- The easiest way to modify the content of an HTML element is by using the innerHTML property

To change the content of an HTML element, use this syntax:
```JavaScript
document.getElementById(id).innerHTML = new HTML;
```

Example:
Changing the content of a `<p>` element
```HTML
<!DOCTYPE html>
<html>
	<body>
		<h2>JavaScript can Change HTML</h2>
		<p id="p1">Hello World!</p>
		
		<script>
			document.getElementById("p1").innerHTML = "New text!";
		</script>

		<p>The paragraph above was changes by a script.</p>
	</body>
</html>
```

Result -> JavaScript can change HTML:
- The paragraph above was changed by a script
```
New text!
```