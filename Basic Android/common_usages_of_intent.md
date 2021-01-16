	- Start an Activity 	--> startActivity(intent)  

	- start a service  --> startService(intent)  

	- deliver a broadcast --> sendBroadcast(intent)  
  		- Intent intent = new Intent(Intant.ACTION_CALL,Uri.parse("tel:"+<Phone_number>))  

  		- Intent intent = new Intent(Intent.ACTION_VIEW,Uri.parse("www.example.com")) // start new activity  

		- startActivity(intent);  