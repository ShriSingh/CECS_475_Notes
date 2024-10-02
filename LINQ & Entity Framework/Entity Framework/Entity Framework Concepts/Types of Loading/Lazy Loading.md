#Week5 
Means that the related data is transparently loaded from the database when the navigation property is accessed
- Default behavior of an Entity Framework
	- A child entity is loaded ***only when it is accessed*** for the 1st time
		- Simply delays the loading of the related data, until you ask for it
		- Can lead to ***multiple database queries***
- Helps optimize database queries by ***loading related data only when it's needed***
	- ***Reduces unnecessary data retrieval***
- Use it when you are sure that you are not using related entities instantly

Examples:
```C#
var customerInvoices = (
	from customer in mmaBooks.Customers  
	where customer.CustomerID == customerID  
	select new { customer.Name, customer.Invoices }
).Single();
```
- A query expression that uses a navigation property to load related objects

```C#
public class Author {
	public int AuthorId { get; set; }
	public string Name { get; set; }
	public virtual ICollection<Book> Books { get; set; }
}

public class Book {
	public int BookId { get; set; }
	public string Title { get; set; }
	public int AuthorId { get; set; }
	public virtual Author Author { get; set; }
}
```
- You have 2 entities, `Author` and `Book`, where `Author` can have multiple `Book` entities associated with them
	1. When you retrieve `Author` entity from the database, ***only the author information is loaded***, and the `Book` collection remains ***empty***
	2. When you access the `Books` ***property***, EF Core will send an additional query to the database to load the related `Book` entities associated with that author
		1. ***Related data is loaded on-demand***
	3. If you want to load related data explicitly in the initial query, you can use the Include method to ***eagerly load*** it

External Links:
https://learn.microsoft.com/en-us/ef/core/querying/related-data/lazy