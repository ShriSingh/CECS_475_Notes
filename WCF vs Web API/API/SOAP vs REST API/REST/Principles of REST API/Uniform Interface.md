#CECS475
#Week7 
This is a fundamental principle for the design of any RESTful API
- There should be uniform and standard way of interacting with a given server for all client types

Constraints that helps achieve this include:
- Identification of resources
	- Every system resource should be uniquely identifiable, by using a Uniform Resource Identifier(URI)
- Manipulation of resources through representations
	- Clients should get a uniform representation of a resource that contains enough information to modify the resource's state in the server
		- As long as they have the required permissions
- Self-descriptive messages
	- Every resource representation should provide enough information for the client to know how to process it further
		- Like additional actions that can be performed on the resources
- Hypermedia as the engine of the application state(HATEOAS)
	- Clients should have enough information, in the form of hyperlinks, to dynamically discover other resources and drive other interactions