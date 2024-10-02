#Week5 
By using "NoTracking", you prevent accidental updates to entities that you didn't intend to modify
- Any changes made to "NoTracking" entities won't be persisted in the database
	- Unless you explicitly attach them to the DbContext in a tracking state