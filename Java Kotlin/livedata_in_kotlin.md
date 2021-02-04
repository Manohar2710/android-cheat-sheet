- LiveData is an `observable` data holder class.

- Unlike regular `observables`, LiveData is `lifecycle-aware`, meaning it respects the lifecycle of an activity, fragment or service.

- This awarness makes sure that LiveData update app component observers that are in active lifecycle state.

- `LiveData` does not have any public method to update the data stored, So we make use of `MutableLiveData` class which exposes the `setValue(T)` and `postValue(T)` to update any data stored in the `LiveData` object.

- Example
```kotlin
class NameActivity : AppCompatActivity() {

	private val model: NameViewModel by viewModels()

	val nameObserver = Observer<String>{ newName ->
		nameTextView.text = newName
	}
	model.currentName.observe(this, nameObserver)
}
class NameViewModel : ViewModel() {

    // Create a LiveData with a String
    val currentName: MutableLiveData<String> by lazy {
        MutableLiveData<String>()
    }

    // Rest of the ViewModel...
}
```