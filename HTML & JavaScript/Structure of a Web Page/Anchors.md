#CECS475 #Week8 
Enable a user to jump to a specific place on a Web site
- 2 steps are necessary to create an anchor
	1. Create the anchor itself
	2. Create a link to the anchor from another point in the document

To create the anchor itself, type:
```HTML
<A NAME="anchor name">label</A>
```
at the point in the Web page where you want the user to jump to

To create the link, type:
```HTML
<A HREF="#anchor name">label</A>
```
at the point in the text where you want the link to appear

Example:
```HTML
<A HREF="#chap2">Chapter Two</A><BR>   <!--Link-->
<A NAME="chap2">Chapter 2</A>          <!--Anchor-->
```
