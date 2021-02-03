- Fragments are part of activity,  

- They provide there own UI when embedded into the activity.  

- An activity can have multiple fragments.  

- fragments are reusable across the activity.  

- Fragment life cycle:  

	- onAttach(Activity) --> Is called when it is attached with acitivity.  

	- onCreate(Bundle) --> is used to initialise the fragment.  

	- onCreateView(LayoutInflator,ViewGroup,Bundle) --> Create and returns view hierarchy.  

	- onActiviyCreate(Bundle) --> is invoked after completion of onCreate method.  

	- onViewStateRestored(Bundle) --> it provides information to the fragments such that all saved state of fragment view hierarchy are restored successfully.  //optional

	- onStart() --> it makes fragments visible.  

	- onResume() --> makes fragment interactive.  

	- onPause() --> is called when fragment is no longer interactive.  

	- onStop() --> is called when fragment is no longer visible.  

	- onDestroyView() --> it allows fragment to clean up `resource`.  

	- onDestroy() --> it allows fragment to clean up of `fragment state`.  

	- onDetach() --> is called when fragment is no longer associated with activity.  