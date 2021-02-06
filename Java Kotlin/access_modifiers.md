- public : 
	- If you dont mention any modifiers, public is used by default.

	- This is widely used in classes, constructors, variables and methods, grants access to any classes and method to anywhere. 

- private :
	- variables, constructors, methods and inner classs are only visible to its containing class and its methods.

	- This variable is used when you want to give access to variables through getters and setters. to maintain encapsulation.

	- `Singleton` constructors is also marked private to avoide any instantiation form outside. 

	- It can only be visible inside the file containing the declaration.

- protected :
	- can only be used on variables, constructors, methods same as private, but will be visible only to class and sub-class.

- internal(Kotlin) :
	- It also called as package private.
	
	- If can class or property declared internal then it is available everywhere in that module.