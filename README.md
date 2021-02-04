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

* **What is Android.?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/What_is_Android.md)
	

* **Who is founder of Android.?**

	- Andy Rubins.

* **What are context? How is it used?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/What_is_Context.md)


* **What are App Components in Android?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/app_components.md)


* **What is the difference between Activity and AppCompatActivity?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/difference_between_Activity_and_AppCompatActivity.md)  


* **Activity, FragmentActivity, AppCompatActivity and ActionBarActivity. How are they related?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/How_are_they_related.md)  


* **Explain Activity life Cycle** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/Explain_Activity_life_Cycle.md)


* **What are Fragments? Describe there lifecycle methods.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/What_are_Fragments.md)


* **Why is it recommended to use default contructor to create a Fragment ?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/Why_Default_Constructor.md)


* **Describe three common usages of intent and how are they invoked and types intent.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/common_usages_of_intent.md)  


* **Define the types of launchMode of an Activity and describe each of them.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/types_of_launchModes.md)   


* **Which method gets invoked when the user presses back button on the screen?**  
	- onbackPressed method is invoked   


* **What is a PendingIntent?**  
	- pendingIntent is an wrapper of Intent. If you want to perform an intent operation at future point on future point of a time on behalf of you, we make use of the pending Intents.   


* **What is a service, Explain?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/What_is_a_service.md) 


* **Define and differentiate between types of services.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/two_types_of_services.md)  


* **Describe the lifecycle methods of a service.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/lifecycle_methods_of_a_service.md)   


* **What is View in Android.? Difference between View.GONE and VIEW.INVISIBLE.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Basic%20Android/View_in_Android.md)


* **Explain View LifeCycyle** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Core%20Android/View_LifeCycyle.md) 


* **What are Canvas?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Core%20Android/what_are_canvas.md) 


* **How does Touch control Event work in Android.?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Core%20Android/what_are_touch_control_event.md)


### Core Android

* **What are Build Type , Product Flavor,Build Variant ?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Core%20Android/Build_Type_Product_Flavor_Build_Variant.md)    


* **What are difference between Room and SQLite ?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Core%20Android/Room_and_SQLite.md) 


* **How does RecyclerView differ from ListView** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Core%20Android/RecyclerView_differ_from_ListView.md)  


* **How to Support Different Screen sizes in Android ?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Core%20Android/Different_Screen_sizes.md) 

		

    
### Android Libraries

#### RXJava

* **Why should we use RxJava on Android?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Android%20Libraries/RxJava_on_Android.md) 


* **What are maps and flatmaps in rxJava?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Android%20Libraries/maps_and_flatmaps_in_rxJava.md) 


### Android Architecture

### Android Design Problem  

### Android Unit Testing  

### Android Tools And Technologies  

### Java Kotlin OOP

#### OOP
* **Explain OOP Concept.** 
	- Object Oriented Programming is methodology used for desiging a program using classes, objects, inheritance, polymorphism, abstraction and encapsulation.

* **Difference between constructor and a method** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/diff_const_and_method.md) 

* **Difference between abstract class and an interface.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/diff_abstract_interface.md)

* **Difference between composition and inheritance** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/diff_composition_inheritance.md)

* **Difference between method overloading and method overiding.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/diff_method_overriding_overloading.md)

* **What are the access modifiers.? Explain each.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/access_modifiers.md)

* **Can an interface implement another interface.?if yes how?**
	- Yes, an interface can implement another interface using the `extend` keyword.

	- And you cannot remove methods from parent interface, but can added new method in the extended interface.

* **What is polymorphism and interface** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/polymorphism_and_inheritance.md) 


#### Kotlin
* **Why kotlin.?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/why_kotlin.md) 

* **Difference between val , var and const.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/diff_val_var_const.md) 

* **What is String Interpolation.?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/string_interpolation.md)

* **Explain init block in kotlin.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/init_block.md)
 
* **Explain init block in kotlin.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/init_block.md)

* **What is an open keyword, where it is used?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/open_keyword.md)

* **What is an open keyword, where it is used?** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/open_keyword.md)

* **What is an Extention function in kotlin.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/extention_function.md)

* **What is an Infix function in kotlin.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/infix_function.md)

* **What is an data class in kotlin.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/data_class.md)

* **What is an Sealed class in kotlin.** [Answer](https://github.com/Manohar2710/android-cheat-sheet/blob/master/Java%20Kotlin/sealed_class.md)


### Data Structures And Algorithms

### Other Topics