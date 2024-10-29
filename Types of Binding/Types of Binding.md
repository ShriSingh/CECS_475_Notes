#CECS475 
#Week6 
- [[Early Binding]]
- [[Late Binding]]

The choice of binding depends on the compiler according to the following rules:
- If a non-virtual element is declared in the hierarchy of inherited classes
	- Early binding is implemented
- If a virtual element is declared in the hierarchy of inherited classes
	- Late binding is performed
	- Virtual Element in the base class is indicated by the `virtual` keyword
		- In all inherited class by the keyword `override`
		- Can be a method, event, indexer, or property in C#
![[Pasted image 20241001193256.png]]

![[Pasted image 20241001193338.png]]
