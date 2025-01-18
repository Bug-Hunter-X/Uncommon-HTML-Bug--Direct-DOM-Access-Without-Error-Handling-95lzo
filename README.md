# Uncommon HTML Bug: Direct DOM Access Without Error Handling

This repository demonstrates a subtle bug in HTML and JavaScript related to accessing DOM elements without proper error handling.  The provided `bug.html` file shows the incorrect way to manipulate a DOM element.  The `bugSolution.html` file provides a corrected implementation that demonstrates how to handle the potential absence of an element.

**Bug:** The original code attempts to access and modify the `innerHTML` of an element with the ID `myDiv`.  If the element with that ID does not exist, this code will throw a runtime error.  This is an uncommon bug as it doesn't produce immediate visible errors but creates unexpected crashes in the browser console.

**Solution:** The solution incorporates a check to see if the element exists before trying to manipulate it.  This prevents the error and ensures graceful degradation.