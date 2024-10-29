#CECS475 
#Week7 
The simplest way to develop and launch a product into the market is to create a website and launch this product
- Develop a website using either ASP.NET MVC, PHP, ASP.NET Core, JSP, etc.
- Use a database such as MySQL, Oracle, SQL Server, etc. to store the entire business data of your product
![[Pasted image 20241013171137.png]]
Combining the website & database, you will have a fully functional dynamic website that interacts with the database. Now if your business grows, you would want to launch an Android/iOS app
- You would now have to create and maintain 3 different applications
	- Even though you have 1 database to store the entire business data
![[Pasted image 20241013171158.png]]

[[Problems without Web APIs]]

Using a Web API can help establish common communication b/w all 3 applications and the database
![[Pasted image 20241013173344.png]]
![[Pasted image 20241013173356.png]]
This way the websites, Android, and iOS applications don't have a *direct access* to the database
- They only need to communicate with the Web API 
	- It's the Web API's responsibility to interact with the database
	- This way the business logic will be written in the Web API
- Acts as a mediator b/w the frontend and the backend