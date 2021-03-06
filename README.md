keyboard-position-fix
==========

This fix addresses flawed virtual keyboard positioning within fixed elements on iOS6 and Android 

Issue
-----

When focusing input elements contained in fixed positioned elements that trigger the virtual keyboard, the screen isn't properly adjusted on iOS6 and Android. 
This makes the UI inusable if the keyboard hides the focused element.  

The issue is described here:

* http://getbootstrap.com/getting-started/#support-fixed-position-keyboards
* http://stackoverflow.com/questions/7970389/ios-5-fixed-positioning-and-virtual-keyboard

Fix
-----------------
The fix hooks in the focusin-event of the document and transforms the position of the fixed parent container on iOS and the body of the document on android.

In iOS7 the issue seems to be resolved and the fix is not applied.
