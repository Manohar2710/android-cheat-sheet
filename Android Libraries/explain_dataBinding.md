- dataBinding is a support library that allows to bind UI components in your layouts to data sources in your app using declarative format rather then programmatically.

- The binding expression allows you to write expressions that connects variables to the views.

- The binding variables that can used as expression will be defined in side an data element that is a sibling of UI layout's root element.

```
<layout xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto">
    <data>
        <variable
            name="viewmodel"
            type="com.myapp.data.ViewModel" />
    </data>
    <ConstraintLayout... /> <!-- UI layout's root element -->
</layout>
```