#Week5 
Means that the related data is loaded from the database as part of the initial query
- Can load the entities by explicitly calling the Load method for the related entities
	- **You have to disable Lazy Loading in an Entity Framework**
- Use it when you're not sure whether or not you'll be using an entity beforehand

Examples:
```C#
var selectedCustomer = (
	from customer in mmaBooks.Customers
	where customer.CustomerID == customerID
	select customer
).Single();

if (!mmaBooks.Entry(selectedCustomer).Collection("Invoices").IsLoaded) {
	mmaBooks.Entry(selectedCustomer).Collection("Invoices").Load();
}
```
- Code that explicitly loads the objects on the *many side of a relationship*

```C#
var selectedInvoice = (
	from invoice in mmaBooks.Invoices
	where invoice.InvoiceID == invoiceID
	select invoice
).Single();

if (!mmaBooks.Entry(selectedCustomer).Reference("Customer").IsLoaded) {
	mmaBooks.Entry(selectedCustomer).Reference("Customer").Load();
}
```
- Code that explicitly loads the object on the *one side of a relationship*

External Links:
https://learn.microsoft.com/en-us/ef/core/querying/related-data/explicit