	- Standard --> Its default launch mode every new instance of activity will be put on top of the stack.  

	- singletop --> if there is an old instance of activity preset in stack.this instance will be called onCreate(), onNewIntent() will be  invoked. if not there will be an new instance created in the stack.  

	- singletask --> on start of this activity all the activities above the task will be cleared similar to standard.  

	- singleInstance -->Similar to singletask espect that for an new activity an new task is created if there are no instance in any task.   