#Week5 
Means writing the LINQ(C#) queries over the entity framework object
- By using these entities, we can perform any operation like insert, delete, update, etc.
Example:
```SQL
Create database db_employee  
use db_employee;

CREATE TABLE [dbo].[EmployeeDetails](  
	[EmpId] INT IDENTITY (1, 1) NOT NULL,  
	[EmpName] VARCHAR (50) NULL,  
	[Location] VARCHAR (50) NULL,  
	[Gender] VARCHAR (20) NULL  
	PRIMARY KEY CLUSTERED ([EmpId] ASC)  
);

INSERT INTO EmployeeDetails(EmpName,Location,Gender) 
	VALUES('Vaishali','Noida','Female');

INSERT INTO EmployeeDetails(EmpName,Location,Gender)
	VALUES('Shalu','Gurgaon','Female');

INSERT INTO EmployeeDetails(EmpName,Location,Gender)
	VALUES('Arpita','Gurgaon','Female');

SELECT * FROM EmployeeDetails;
```
- After executing the above query. The table will show the data, as shown below:

|     | EmpID | EmpName  | Location | Gender |
| --- | ----- | -------- | -------- | ------ |
| 1   | 1     | Vaishali | Noida    | Female |
| 2   | 2     | Shalu    | Gurgaon  | Female |
| 3   | 3     | Arpita   | Gurgaon  | Female |
- We need to add an ADO.NET Entity Data Model(EDM) in our application to use Entity with LINQ
	- [[Adding ADO.NET EDM]]
