- When we touch the screen, the activities view gets touch event notification first, also knows as `DecoView`.

- The Touch event is passed from Top to Bottom hierarchy of ViewGroup to children using dispatchTouchEvent().

- To Intercept the touch event we make use of the function called onIntercetTouchEvent().

- If we return true on Intercept then the event is not passed, similarly on returning false the touch event are transfard to children view.