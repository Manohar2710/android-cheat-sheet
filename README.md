# Android Interview QA

**1) What is Android.?**

It is an open source operating system that is primarily used on mobile devices,such as cell phones and tablets.  
It is an kernel linux based operating system that allows developers to create and run apps that can perform basic and advanced functions.


**2) Who is founder of Android.?**

Andy Rubins.


**3) What are app components in Android?**

App Component are Essential Building blocks of android.Each component are starting or entry point through\ which the system or user can enter the app.Some component depend on others.

There are 4 different types of app components.

	* Activities - An activity is an entry point for interacting with the user.It represents a single sreen with a user interface.

	* Services - An service is an general-purpose entry point for keeping an app running for app kind of reasons.

	* Broadcast Receivers - It is an component that enables system to deliver events to app outside of a regular user flow.
	
	* content providers - manages shared set of app data that you can store in file system,in a SQLite database ,on web,on a persistent storage that your app can access


**4) What is the difference between Activity and AppCompatActivity?**  
	Ans : a) AppCompactActivity provides nativve actionbar that is consistent accross the application.  
		  b) it provides backward compatibility for other design material components till SDk 7.  
		  c) SDK 21 every activity by default extends AppCompactActivity.  


**5) Activity, AppCompatActivity, FragmentActivity and ActionBarActivity. How are they related?**  
	Ans : a) Activity is the base class.  
		  b) FragmectsActivity extends Activity.  
		  c) AppCompactActivity Extents FragmentsActivity.  
		  d) ActionBarActivity Extends AppCompactActivity.  

**6) Explain Activity life Cycle:**
	Ans :  

	onCreate() --> This method is first invoked when the activity is launched 

	onStart() --> This method is invoked when the after the onCreate() complete its task.  

	onResume() --> this method is called after onStart().  

	onPause() --> This method is called when the activity leaves the foreground(standby/sleep).  

	onStop() --> This is method is invoked when the activity is not visible anymore(another activity is launched)  

	onDestroy() --> this method is called when the activity or application is destroyed.  

	onRestart() -->   

**7) What are Fragments? Describe there lifecycle methods.**  
	Ans : Fragments are part of activity,  
		  They provide there own UI when embedded into the activity.  
		  An activity can have multiple fragments.  
		  fragments are reusable across the activity.  

		  Fragment life cycle:  

		  onAttach(Activity) --> Is called when it is attached with acitivity.  

		  onCreate(Bundle) --> is used to initialise the fragment.  

		  onCreateView(LayoutInflator,ViewGroup,Bundle) --> Create and returns view hierarchy.  

		  onActiviyCreate(Bundle) --> is invoked after completion of onCreate method.  

		  onViewStateRestored(Bundle) --> it provides information to the fragments such that all saved state of fragment view hierarchy are restored successfully.  

		  onStart() --> it makes fragments visible.  

		  onResume() --> makes fragment interactive.  

		  onPause() --> is called when fragment is no longer interactive.  

		  onStop() --> is called when fragment is no longer visible.  

		  onDestroyView() --> it allows fragment to clean up resources.  

		  onDestroy() --> it allows fragment to clean up of fragment state.  

		  onDetach() --> is called when fragment is no longer associated with activity.  


**8) Describe three common usages of intent and how are they invoked and types intent.**  
	Ans : a) Start an Activity 	--> startActivity(intent)  
		  b) start a service  --> startService(intent)  
		  c) deliver a broadcast --> sendBroadcast(intent)  

		  Intent intent = new Intent(Intant.ACTION_CALL,Uri.parse("tel:"+<Phone_number>))  
  		  Intent intent = new Intent(Intent.ACTION_VIEW,Uri.parse("www.example.com")) // start new activity  
		  startActivity(intent);  


**9) Define the types of launchMode of an Activity and describe each of them.**  
	Ans : Standard --> Its default launch mode every new instance of activity will be put on top of the stack.  
		  singletop --> if there is an old instance of activity preset in stack.this instance will be called onCreate(), onNewIntent() will be  invoked. if not there will be an new instance created in the stack.  
		  singletask --> on start of this activity all the activities above the task will be cleared similar to standard.  
		  singleInstance -->Similar to singletask espect that for an new activity an new task is created if there are no instance in any task.   

**10) Which method gets invoked when the user presses back button on the screen?**  
	Ans : onbackPressed method is invoked   


**11) What is a PendingIntent?**  
	Ans : pendingIntent is an wrapper of Intent. it is passed to an fourign application(Notification ,alarm) such that when some given condition is met the desired action is performed on the intent object it holds onto.  

**12) What is a service?**  
	Ans : a) Its is an component in android used for performing task in background such as play music location update.  
		  b) Unlike activities service doesnt have an UI.    
		  c) an service keeps running in backgroung even after the activities are destroyed.  

**13) Define and differentiate between the two types of services.**  
	Ans : a) Bound Service  
			--> an android component can bind itself using bindService().  
			--> an bound service would run as long as the other application component are bound to it.  
			--> we can use unBineService() to unbind the service from that activity.  

		  b) UnBoundService  
		  	--> it starts when a activity calls startActivity method.  
		  	--> it runs background even after the original component is destroyed.   

**14) Describe the lifecycle methods of a service.**  
	Ans : startService()         	bindService()  
				|						|  
			onCreate()				onCreate()  
				|						|  
		 OnStartCommand()			 onBind()  
		 		|						|  
		service is running		service is running  
				|						|  
			OnDestroy()				onUnbind()  
				|						|  
		service is stopped			onDestroy()  
										|  
								service is stopped  
		

**15) Why should we use RxJava on Android?**  
	Ans :   
		a)We use RxJava for multithreading  
		a)subscribOn(Scheduler.io()) --> will process everything in a new thread.  
		b)observeOn(Schedulers.Mainthread()) --> will listen to results on main thread.  
		c)filter() --> Used to filter result data   
		d)subscribe() -->   
		e)we can join the results of two data object in the result  

**16) What are maps and flatmaps in rxJava?**  
	Ans :   
		Map :  
			a)Map transforms the items emitted by an observable by applying a function to each of them.  
		FlatMap :  
			b) flatmap tansforms the items emitted by observable in observables.  
			c) Very important: FlatMap is used to map over asynchronous operations.  