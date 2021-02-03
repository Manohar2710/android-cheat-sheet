- It is the context of `current state` of application.

- Used to get info regarding `Activity` and `Application`.

- Used to get info regarding the shared preferences, resources and databases ect.

- Two types of context 
	- Application context.
		- It is an `SingleTon instance`.

		- Access using the method `getApplicationContext()`.
	
	- Activity context.
		- It is available in the activity.

		- It is attached to the lifecycle of the activity.