	- `View` class Represents the basic building blocks for User Interface Components.

	- A view occupies an `Rectangular area` on the screen, and is responsible for drawing and Event handling.

	- View is base class of `widget`.

	- Below is lifecycle of view class which undergoes several methods to get drawn on the screen.

	![](./res/view_lifecycle.png "View lifecycle")

	- Explanation
		- `onAttachedToWindow()`- Called when a view is attached to window,this is when the view knows it can be active and has surface for drawing.
		- `onFinishInflate()`- Called when a view and all of its children are inflated from XML.
		- `onMesure(Int,Int)`- Determines the size requirements for this view and all of its children.
		- `onLayout()`- Called when this view should assign the size and position to all of its children.
		- `onSizeChanged()`- Called when the size of view has changed.
		- `onDraw(android.graphics.Canvas)`- Canvas object generated(or updated) has list of OpenGL_ES commands (displayList) to send to GPU.
		- `invalidate()`- method that insist redrawing a perticular view that we wish to show changes.
		- `reuestLayout()`- At some point, there is a state change in view, requestLayout() is the signal to system that it needs to recalculate the measures and layout phase of the views.
		- `onDispatchFromWindow()`- This is called when view is detached from the a window.  