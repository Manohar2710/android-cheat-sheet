- By default all the classes in kotlin are final in nature, as we know that an final class cannot be inherited to any classes or interface, we have to use keyword open to make the class inheritable.

- Similarly the properties of a class i.e. funations and variables are by default defined as final, here we make use of open keyword to make the properties inheritable.

- Example 
	```kotlin
	open class SampleClass{

		open val sampleVal:Int = 0
		
		open fun sampleFunction(){
			...
		}
	}
	```
