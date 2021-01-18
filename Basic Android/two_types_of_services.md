	- Bound Service  
		- an android component can bind itself using bindService().  
		- an bound service would run as long as the other application component are bound to it.  
		- we can use unBineService() to unbind the service from that activity.  

  	- UnBoundService  
		- it starts when a activity calls startActivity method.  
		- it runs background even after the original component is destroyed.   