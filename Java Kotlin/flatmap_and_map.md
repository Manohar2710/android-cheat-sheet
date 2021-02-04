- map : 
	- Map returns a list containing of results applying the certain set of tranformation to each element in the original collection.

	- in general terms, flat map is used to modify the list according to our requirments.

	```kotlin
	val numbers = listOf(1,2,3,4,5)
	squaredNumbers = numbers.map{
		it * it
	}
	```

- flatMap : 
	- flatMap returns a list of all elements yielded from results of applying certain condition on each element of original collection.

	- in general terms, flatMap is used to yield or combide two different collection and return single collection.

	```kotlin
	val cars = listOf(
		MotorVehicle("Swift",2019)
		MotorVehicle("Swift",2019)
		)
	val bikes = listOf(
		MotorVehicle("R-15",2018)
		MotorVehicle("discover",2016)
		)
	val allVehicles = listOf(cars,bikes).flatMap { it }
	```