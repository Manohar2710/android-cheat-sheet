- Foreground Service 
	- This is something which is noticeable to the user .Ex Audio app to use Foregroudservice to change the track

	- It must display notification.

- UnBoundService(BackgroundSerive)  
	- it starts when a activity calls `startService()` method.  
	
	- it runs background even after the original component is destroyed.   

- Bound Service  
	- an android component can bind itself using bindService().  

	- an bound service would run as long as the other application component are bound to it.  

	- we can use unBineService() to unbind the service from that activity.  

