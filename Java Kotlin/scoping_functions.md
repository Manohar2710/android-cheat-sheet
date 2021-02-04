- Basically all this functions to the same i.e. to execute a block of code on an object, but the diffeence is how this object becomes available innside the block and what is the result of the whole expression.

- The default object name inside the lambda scope will be `this` or `it`

- The scopes `with`, `apply` and `run` represents as `this`.

- The scopes `let` and also represents as `it`.

- There are 5 of them:
	- let :
		- The context object is available as argument `it`.The return value is the lambda result.

		- let can be used to invoke one or functions on results of call chains.

		- let is also used for executing block of code only with not-null values,by using the safe call operator `?.` on the nullable variable. 

		- Example
		```kotlin 
		val numbers = mutableListOf("one", "two", "three", "four", "five")
		numbers.map { it.length }.filter { it > 3 }.let { 
		println(it)
		// and more function calls if needed
		} ```

	- with : 
		- The context object is passed as an argument, but inside the lambda, its available as `this`, the return value is lambda result.

		- It can be read as `with this object do the following`.

		- Example
		```kotlin
		val numbers = mutableListOf("one", "two", "three")
		with(numbers) {
		    println("'with' is called with argument $this")
		    println("It contains $size elements")
		}
		```

	- run :
		- The context object is available as a receiver(`this`),The return value is lambda result.

		- `run` does the same as `with` but invokes as `let`

		- `run` is usefull when you want to perfrom both initialization and computation inside the lambda.

		- Example
		```kotlin
		val service = MultiportService("https://example.kotlinlang.org", 80)
		val result = service.run {
	    port = 8080
	    query(prepareRequest() + " to port $port")
		}
		``` 

	- apply : 
		- context object is available as a receiver `this`,The return value is the object itself.

		- `apply` is basically used run code of blocks that don't return a value,but mainly operate on the members of the object.

		- Exmaple
		```kotlin
		val adam = Person("Adam").apply {
	    	age = 32
	    	city = "London"        
		}
		println(adam)
		```

	- also :
		- context object is available as a receiver(`this`),the return value is the object itself.

		- also is also read as `and also do the following with the object`

		- Example
		```kotlin
		val numbers = mutableListOf("one", "two", "three")
		numbers
    		.also { println("The list elements before adding new one: $it") }
    		.add("four")
		```
