#Week5 
- Provides: database connected to application -- Layer -- objects in the application
	- An interface that allows data in the database to be presented to the application as objects
- Interface is provided using the *Entity Data Model* that defines a 
	- [[Conceptual model]]
	- Storage model
	- Mappings b/w the two models
- When you execute a query against a conceptual model
	- *Object Services* works with the *EntityClient data provider* and the Entity Data Model to translate the query into one that can be executed by the database
	- When the results are returned from the database
		- Object Services translates them back to the objects defined by the conceptual model
- Assists in tracking changes and for submitting those changes to the database

[[Entity Framework Core]]
