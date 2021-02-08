- View binding is a feature that allows us to more easily interact with views.

- Once view binding is enabled in module, it generates a binding class for each XML layout file present in module.

- Setup

	- To enable view binding in a module, set the viewBinding build option to true in the module-level build.gradle.

	- Exmaple
	```kotlin
	android{
		...
		buildFeatures{
			viewBinding ture
		}
	}
	``` 

	- Usage in activity 
	````kotlin
	private latinit var _binding = ResultProfileBinding

	override fun onCreate(savedInstanceState : Bundle?){
		super.onCreate(savedInstanceState)
		_binding = ResultProfileBinding .inflate(layoutInflatrer)
		val view = _binding.root
		setContentView(view)
	}
	```


	- Usage in Fragment
	```kotlin
	private latinit var _binding = ResultProfileBinding
	override fun onCreateView(
	    inflater: LayoutInflater,
	    container: ViewGroup?,
	    savedInstanceState: Bundle?
	): View? {
	    _binding = ResultProfileBinding.inflate(inflater, container, false)
	    val view = binding.root
	    return view
	}
	``` 