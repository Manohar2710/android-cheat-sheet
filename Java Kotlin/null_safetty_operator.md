- In kotlin, the type system distinguishes between references that can hold null,and that cannot hold null.
```kotlin
var a : String = "abc"
a = null // compilation error
```
- To declare an variable as nullable strings i.e. String?
```kotlin
var a : String? = "abx"
a = null // ok
```
- we have safe call technique to check weather an reference has null value.
```kotlin
val a:String? = "kotlin"
print(a?.length) // prints null
```
- we can use the safe call operator together with `let`
```kotlin
val listWithNulls: List<String?> = listOf("Kotlin", null)
for (item in listWithNulls) {
    item?.let { println(it) } // prints Kotlin and ignores null
}
```