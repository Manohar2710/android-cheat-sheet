- Data class 
	- The boiler plate POJO code in java are converted to data class in Kotlin.

- Null safety
	- kotlin does not let us initialise an null to an variable until its diclared as nullable type.

	- Example : 
		```kotlin
		var myName : String 
		myName = null // compilation error

		// use the nullable feature
		var myName : String? = null
		println(myName.length) // compilation error	
		```


- Interoperability
	- Java classes can be easily used or instantiated in a kotlin code with any compilation or run time error.

- String interpolation 
	-  Concatination string made easier, where in java we need the append function to concatinate, in kotlin we use string interpolation technique.
	- Example
		```
		val s = "Today is a sunny day."
		println("The string has ${s.length} characters")
		```

- Concise 
	- you are able to solve same problem from java with fewer lines of code.

	- Some kotlin features that are responsible for there conciseness are.
		- Data classes

		- Smart cast

		- type interface

		- properties 