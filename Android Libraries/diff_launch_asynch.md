- These are the main two function available to start the coroutines

- Launch :
	- It will not block the main Thread, but the execution of the other lines of code will not be effected,As launch is not a suspend call.

	- can be called as fire and forget.

	- launch can be used inside a normal function.

	- Example
	```kotlin 
	fun launchExample(){ 
  		var resultOne = "Android"
		var resultTwo = "Kotlin"
		Log.i("Launch", "Before") 
		launch(Dispatchers.IO) { resultOne = function1() } 
		launch(Dispatchers.IO) { resultTwo = function2() } 
		Log.i("Launch", "After") 
		val resultText = resultOne + resultTwo 
		Log.i("Launch", resultText) 
	} 
  
	suspend fun function1(): String { 
		delay(1000L) 
		val message = "function1"
		Log.i("Launch", message) 
		return message 
	} 
  
	suspend fun function2(): String { 
		delay(100L) 
		val message = "function2"
		Log.i("Launch", message) 
		return message 
	}

	//Output
	Launch : Before
	Launch : After
	Launch : AndroidKotlin // wont wait for result as it is not in main thread.
	Launch : function2 // function2 exetutes first as it has less delay
	Launch : function1
	```


- Async :
	- Async is also used to start a coroutines, but it block the main thread at the entry point of the `await()` function in the program.

	- Allows you to return a result, when used with the suspend function and await.

	- Asynch should be called inside a coroutines scope.

	- Example 
	```kotlin
	fun asyncExample()  { 
		Log.i("Async", "Before") 
		val resultOne = Async(Dispatchers.IO) { function1() } 
		val resultTwo = Async(Dispatchers.IO) { function2() } 
		Log.i("Async", "After") 
		val resultText = resultOne.await() + resultTwo.await() 
		Log.i("Async", resultText) 
	} 
  
	suspend fun function1(): String  
	{ 
		delay(1000L) 
		val message = "function1"
		Log.i("Async", message) 
		return message 
	} 
  
	suspend fun function2(): String  
	{ 
		delay(100L) 
		val message = "function2"
		Log.i("Async", message) 
		return message 
	}

	// output
	Async : Before
	Async : After
	Async : function2
	Async : function1
	Async : function1function2
	```