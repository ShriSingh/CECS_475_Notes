Enable a class or object to notify other classes or objects when some action occurs
- Used to trigger a function
	- Action could be anything:
		- User clicking a button to finish loading a webpage
- Helps make program interactive and responsive to user input
- A wrapper around a delegate
	- Depends on the delegate
- Register an event with `+=` operator
	- Can't do it with `=` operator
- Unsubscribe an event with `-=` operator

Two parts of an event:
- [[Publisher]]
- [[Subscriber]]

[[Properties of an Event]]

Event is an encapsulated delegate
- Dependent on the delegate
	- Delegate defines the signature for the event handler method of the subscriber class
		- Signature of the handler method must match the delegate signature
- [[Built-in EventHandler Delegates]]

[[Declaring an Event]]

[[Raising an Event]]

[[Consume an Event]]

[[Passing an Event]]



