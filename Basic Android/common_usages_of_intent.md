- To Start an Activity 	--> startActivity(intent)  

- To Start a service  -->  startService(intent)  

- To Deliver a broadcast --> sendBroadcast(intent)  

- An Intent is also used as an means of data transfer technique between the components.

- Example :
	- Intent intent = new Intent(Intant.ACTION_CALL,Uri.parse("tel:"+<Phone_number>))  

	- Intent intent = new Intent(Intent.ACTION_VIEW,Uri.parse("www.example.com")) // start new activity  

	- startActivity(intent);  

- Types of Intent
	- Explicit Intent :
		-  If you want to start new activity using the component name we make use of explicit intent.

		- we have to provide fully defined address of the component to launch.

		- Example : 
		```kotlin
		val intent = Intent(this,NewActivity::class.java)
		intent.data = Uri.parse(fileURL)
		startActivity(intent)
		```

	- Implicit Intent : 
		- If you want a `perticular action` to be perfomed from external application, we make use of implicit intent.

		- for example if you want to `send a message`, then the Android system will provide Gmail,Instagram,Whatsap etc options.

		- Example : 
			```kotlin
			val intent = Intent().apply{
				action = Intent.ACTION_SEND
				putExtra(Intent.EXTRA_TEXT,textMessage)
				type = "text/plain"
			}
			//Verifying that the intent resolves to an activity
			if(intent.resolveAvtivity(packageManager) != null){
				startActivity(intent)
			}
			```
