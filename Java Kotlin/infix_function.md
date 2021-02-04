- If an function is declared with Infic keyword, we can call that function without using the dot and the parantheses.

- Example
	```kotlin 
		infix fun samplefun(val type:String ): String {
			return "this is a $type function"
		}

		val result = samplefun "infix"
		print(result) // this will print as "this is a infix function"
	```