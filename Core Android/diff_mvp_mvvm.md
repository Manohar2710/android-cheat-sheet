|      MVP      |      MVVM       |
|---------------|-----------------|
| model view presenter| model view view model|
| presenter contains the business logic|view model contains the business logic|
| low XML complexity| high XML complexity|
| Good Unit testing| Great Unit testing|
| one-to-one relationship between view and presenter|many to one relationship between view and viewmodel |
| Auto-UI update is not present here| Using LiveData class with observer in the activity, Auto-Ui update is possible |
| view and presenter are tightly coupled| view and presenter are loosely coupled |
| Light Weight|heavy weight|