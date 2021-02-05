- From Activity to Activity : 
	```kotlin
	val intent = Intent(this,SecondActivity::class.java)
	intent.putExtra("message",message)
	startActivity(intent)
	```

- From Activity to Fragment : 
	```kotlin
	val bundle = Bundel()
	bundle.putString("message",message)
	val fragmentClass = FragmentClass()
	fragmentClass.setArguments(bundle)

	//To receive it in fragment
	val message = getArguments().getString("message")
	```