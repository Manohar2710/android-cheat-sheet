- Default : 
	- This modifier is applied to classes, variables, constructors and methods and allows access from classes and methods inside the same package.

- public : 
	- This is widely used in classes, constructors, variables and methods, grants access to any classes and method to anywhere. 

- private 
	- variables, constructors, methods and inner classs are only visible to its containing class and its methods.

	- This variable is used when you want to give access to variables through getters and setters. to maintain encapsulation.

	- Singleton constructors is also marled private to avoide any instantiation form outside. 

- protected 
	- can only be used on variables, constructors, methods. Hence allowing access only to class and sub-class that are inside the same package as protected member class.

- internal(Kotlin) :