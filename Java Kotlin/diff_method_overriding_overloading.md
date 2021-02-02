|     Method Overriding     |    Method Overloading      |
|---------------------|----------------|
| Method overloading happens at compile time | Method Overriding happens at run time|
| For overriding both base class and child class are required|overloading is done in same class|
| Private and final methods can not be overrided |In case f overloading it is possible|
| Argument of the method should be same |Argument of the method should be different here|

- Example  

	```java
	public class Animal {
		public static void testClassMethod(){
			System.out.println("public class method in Aminal")
		}
		public void testInstanceMethod(){
			Syste,out.println("public instance method in Animal ")
		}
	} 
	public class Cat extends Animal {
		public static void testClassMethod(){
			System.out.println("public class method in Cat")
		}
		public void testInstanceMethod(){
			Syste,out.println("public instance method in Cat ")
		}
	    public static void main(String[] args) {
	        Cat myCat = new Cat();
	        myCat.testClassMethod();
	        Animal myAnimal = myCat;
	        myAnimal.testClassMethod();
	        myAnimal.testInstanceMethod();
    	}
	}
	```
	- OutPut  

	```
	public class method in Cat // method testClassMethod is called of Cat reference.
	public class method in Aminal // method testClassMethod is called of Animal reference.
								// ignoring the actual method inside the Cat class.
	public instance method in Cat // method public instance method is called in Cat 
								// the method in Animal class is ignored.
	```