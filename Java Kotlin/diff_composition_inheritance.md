- Composition :
	- Composition is a design technique in object oriented programming to implement `has-a` relationship between the objects.

	- Composition is loosely coupled.

	- Example : 
		```java
		public class Job {
			...
		}
		public class person{
			private Job job;
		}
		```
	- In the above example the person has a job object which shows the example for the composition has-a relationship.

- Inheritance
	- Inheritance is a design technique in object oriented programming to implement is-a relationship between objects.

	- Inheritance is tightly coupled.

	- Example : 
		```java
		public class Emplyoed{
			//super classs
		}
		public class Person extents Employed{
			//sub class
		}
		```
	- Inheritance being tightly coupled, This is over come by `default` method technique in Java.

	- For kotlin we make use of the `@JvmDefault` method to over come the tightly coupled issue in interface.