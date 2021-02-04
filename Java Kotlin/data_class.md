- Its primary constructor needs to have atleast one parameter.

- All primary constructor parameters needs to be marked as val or var.

- data class cannot be sealed/abstract/open/inner.

- optional parameters need to declared last in the primary constructor.

- Example
```kotlin
data class Student(
	val name : String, 
	var age : Int
)
```