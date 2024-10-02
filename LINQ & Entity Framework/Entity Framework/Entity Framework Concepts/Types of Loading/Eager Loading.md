#Week5 
Means that the related data is loaded from the database as part of the initial query
- Helps you to load all your needed entities at once, ***along with the main entity in a single database query***
	- All you child entities will be loaded in a single database call
		- Achieved using `Include` method
			- Returns the related entities as a part of the query
			- A large amount of data is loaded at once
- Helps improve performance by reducing the database round trips
	- When dealing with complex object graphs
- Use it when the relations are not too much
	- A good practice to reduce further queries on the Server
- Use it when you are sure that you'll be using related entities with the main entity everywhere

Examples:
```C#
var selectedCustomer = (
	from customer in mmaBooks.Customers.Include("Invoices")
	where customer.CustomerID == customerID
	select customer
).Single();
```
- A query expression that uses the `include` method to load related objects

```C#
using(var context = new YourDbContext()) {
	var authorWithBooks = context.Authors
		.Include(a => a.Books) // Specify the related entity to load
		.FirstOrDefault(a => a.Name == "J.K. Rowling");
	// Now, authorWithBooks.Books contains the related books, and they were loaded in a single query
}
```
- `Include` method is used to specify the related entity(`Books`) that you want to load eagerly

External Links:
https://learn.microsoft.com/en-us/ef/core/querying/related-data/eager