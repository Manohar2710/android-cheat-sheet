# Android Interview Questions

## Contents
* [Basic Android](#basic-android)
* [Core Android](#core-android)
* [Android Libraries](#android-libraries)
* [Android Architecture](#android-architecture)
* [Android Design Problem](#android-design-problem)
* [Android Unit Testing](#android-unit-testing)
* [Android Tools And Technologies](#android-tools-and-technologies)
* [Java and Kotlin](#java-and-kotlin)
* [Data Structures And Algorithms](#data-structures-and-algorithms)
* [Other Topics](#other-topics)

### Basic Android

* **What is Android.?**
	- It is an open source operating system that is primarily used on mobile devices,such as cell phones and tablets.It is an kernel linux based operating system that allows developers to create and run apps that can perform basic and advanced functions.


* **Who is founder of Android.?**

	- Andy Rubins.


* **What are app components in Android?**
	- App Component are Essential Building blocks of android.Each component are starting or entry point through\ which the system or user can enter the app.Some component depend on others.

	- There are 4 different types of app components.

		- Activities - An activity is an entry point for interacting with the user.It represents a single sreen with a user interface.

		- Services - An service is an general-purpose entry point for keeping an app running for app kind of reasons.

	  	- Broadcast Receivers - It is an component that enables system to deliver events to app outside of a regular user flow.
	
		- content providers - manages shared set of app data that you can store in file system,in a SQLite database ,on web,on a persistent storage that your app can access


* **What is the difference between Activity and AppCompatActivity?**  
	- AppCompactActivity provides nativve actionbar that is consistent accross the application.  

	- it provides backward compatibility for other design material components till SDk 7.  

	- SDK 21 every activity by default extends AppCompactActivity.  


* **Activity, AppCompatActivity, FragmentActivity and ActionBarActivity. How are they related?**  
	- Activity is the base class.  

	- FragmectsActivity extends Activity.  

	- AppCompactActivity Extents FragmentsActivity.  

	- ActionBarActivity Extends AppCompactActivity.  


* **Explain Activity life Cycle:**
	- onCreate() --> This method is first invoked when the activity is launched 

	- onStart() --> This method is invoked when the after the onCreate() complete its task.  

	- onResume() --> this method is called after onStart().  

	- onPause() --> This method is called when the activity leaves the foreground(standby/sleep).  

	- onStop() --> This is method is invoked when the activity is not visible anymore(another activity is launched)  

	- onDestroy() --> this method is called when the activity or application is destroyed.  

	- onRestart() -->   


* **What are Fragments? Describe there lifecycle methods.**  
	- Fragments are part of activity,  

	- They provide there own UI when embedded into the activity.  

	- An activity can have multiple fragments.  

	- fragments are reusable across the activity.  

	- Fragment life cycle:  

		- onAttach(Activity) --> Is called when it is attached with acitivity.  

		- onCreate(Bundle) --> is used to initialise the fragment.  

		- onCreateView(LayoutInflator,ViewGroup,Bundle) --> Create and returns view hierarchy.  

		- onActiviyCreate(Bundle) --> is invoked after completion of onCreate method.  

		- onViewStateRestored(Bundle) --> it provides information to the fragments such that all saved state of fragment view hierarchy are restored successfully.  

		- onStart() --> it makes fragments visible.  

		- onResume() --> makes fragment interactive.  

		- onPause() --> is called when fragment is no longer interactive.  

		- onStop() --> is called when fragment is no longer visible.  

		- onDestroyView() --> it allows fragment to clean up resources.  

		- onDestroy() --> it allows fragment to clean up of fragment state.  

		- onDetach() --> is called when fragment is no longer associated with activity.  


* **Describe three common usages of intent and how are they invoked and types intent.**  
	- Start an Activity 	--> startActivity(intent)  

	- start a service  --> startService(intent)  

	- deliver a broadcast --> sendBroadcast(intent)  
  		- Intent intent = new Intent(Intant.ACTION_CALL,Uri.parse("tel:"+<Phone_number>))  

  		- Intent intent = new Intent(Intent.ACTION_VIEW,Uri.parse("www.example.com")) // start new activity  

		- startActivity(intent);  


* **Define the types of launchMode of an Activity and describe each of them.**  
	- Standard --> Its default launch mode every new instance of activity will be put on top of the stack.  

	- singletop --> if there is an old instance of activity preset in stack.this instance will be called onCreate(), onNewIntent() will be  invoked. if not there will be an new instance created in the stack.  

	- singletask --> on start of this activity all the activities above the task will be cleared similar to standard.  

	- singleInstance -->Similar to singletask espect that for an new activity an new task is created if there are no instance in any task.   


* **Which method gets invoked when the user presses back button on the screen?**  
	- onbackPressed method is invoked   


* **What is a PendingIntent?**  
	- pendingIntent is an wrapper of Intent. it is passed to an fourign application(Notification ,alarm) such that when some given condition is met the desired action is performed on the intent object it holds onto.  


* **What is a service?**  
	- Its is an component in android used for performing task in background such as play music location update.  

	- Unlike activities service doesnt have an UI.    

	- an service keeps running in backgroung even after the activities are destroyed.  


* **Define and differentiate between the two types of services.**  
	- Bound Service  
		- an android component can bind itself using bindService().  
		- an bound service would run as long as the other application component are bound to it.  
		- we can use unBineService() to unbind the service from that activity.  

  	- UnBoundService  
		- it starts when a activity calls startActivity method.  
		- it runs background even after the original component is destroyed.   


* **Describe the lifecycle methods of a service.**  
	- UnBound Service  
		- startService()         	
							
		- onCreate()				
									
		- OnStartCommand()		
		 						
		- service is running	
								
		- OnDestroy()				
									
		- service is stopped			
	
	- UnBound Service							
		- bindService()   						
		
		- onCreate()  

		- onBind()  

		- service is running

		- onUnbind()

		- onDestroy()

		- service is stopped  


### Core Android

* **What are Build Type , Product Flavor,Build Variant ?**
	- Build type
		- Build type controls how to build packages of your app.

		- the build system defines two build types `debug` and `release`.
		```
	    buildTypes {
	        release {
	            minifyEnabled false
	            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
	        }
	        debug{
	        	applicationIdSuffix ".debug"
	        }
	        /**
	         *The `initWith` property allows to copy configurations from other build types.
	         *This copies the debug build type and changes the manifestplaceholder and applicationIdSuffix
	         */
	        staging{
	        	initWith debug
	        	manifestPlaceHolders = [hostName:"internal.example.com"]
	        	applicationIdSuffix ".debugStaging"
	        }
	    }
		```
	- Product Flavours
		- Product flovours provide a customized version of the application build.

		- It is used to define custom features , minimum and target API levels.

		- This can help create different labeled apps as well.

		```
		flavourDimensions "version"
		productFlovours {
			demo {
				dimension "version"
				applicationIdSuffix ".demo"
				versionNameSuffix "-demo"
			}
			full {
				dimension "version"
				applicationIdSuffix ".full"
				versionNameSuffix "-full"
			}
		}
		```
	- Build varient 
		- The Combination of Build types and product flavours is known as Build Varient.

		- For the above build types (debug and release) and product flavour (demo and full version), build varient can be `demoDebug`,`demoRelease`,`fullDebug` and `fullRelease`.

* **What are difference between Room and SQLite?**
	- SQLite
		- SQLite is a in-process library that contains self-contained, serverless, zero-configuration, transactional SQL Database.

		- SQLite is anembedded SQL databse engine.

		- SQLite Reads and write data directly to ordinary disc files.

		- The Databare file formate is cross-platform(copy between 32 to 64 bit system).

		- There is no SQL queries validation during the compile time.

		- Lot of boiler plate code to convert SQL quries to Java object

		- It does not support RXjava or any reactive frame works

	-Room
		- Room persistence library provides an abstraction layer over the SQLite to allow more robust database access.

		- This helps you to create an cache of your app data on the device thats running your app.

		- Room is an ORM (Object Relational mapping library). This will map our database object to java objects.

		- There is an SQL queries validation at compile time.

		- Lesser code to convert SQL queries to Java object.

		- Room is built to work with live data and RXjava for data observation.



### Android Libraries

#### RXJava

* **Why should we use RxJava on Android?**    
	- We use RxJava for multithreading  

	- subscribOn(Scheduler.io()) --> will process everything in a new thread.  

	- observeOn(Schedulers.Mainthread()) --> will listen to results on main thread.

	- filter() --> Used to filter result data   

	- subscribe() -->   

	- we can join the results of two data object in the result  


* **What are maps and flatmaps in rxJava?**  
	- Map   
		- Map transforms the items emitted by an observable by applying a function to each of them.  

	- FlatMap :  
		- flatmap tansforms the items emitted by observable in observables.  

		- Very important: FlatMap is used to map over asynchronous operations.  


#### Android Architecture

#### Android Design Problem  

#### Android Unit Testing  

#### Android Tools And Technologies  

#### Java and Kotlin

#### Data Structures And Algorithms

#### Other Topics