#CECS475 #Week8 
A tree structure whose nodes represent an HTML or XML document's contents
- Includes elements such as `<body>` and `<table>` etc.
- Provides functionality globally to the document
	- Like how to obtain the page's URL
	- Like create new elements in the document
Example:
For the following document,
```HTML
<html lang="en">
	<head>
		<title>My Document</title>
	</head>
	<body>
		<h1>Header</h1>
		<p>Paragraph</p>
	</body>
</html>
```

A DOM tree could look like:
![[using_the_w3c_dom_level_1_core-doctree.jpg]]
