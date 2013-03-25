# Module: dijit/_base/focus

## Summary

Deprecated module to monitor currently focused node and stack of currently focused widgets.
New code should access dijit/focus directly.
## Methods

### getBookmark
Retrieves a bookmark that can be used with moveToBookmark to return to the same range

### getFocus
Called as getFocus(), this returns an Object showing the current focus
and selected text.

Called as getFocus(widget), where widget is a (widget representing) a button
that was just pressed, it returns where focus was before that button
was pressed.   (Pressing the button may have either shifted focus to the button,
or removed focus altogether.)   In this case the selected text is not returned,
since it can't be accurately determined.


### isCollapsed
Returns true if there is no text selected

### moveToBookmark
Moves current selection to a bookmark

### registerIframe
Registers listeners on the specified iframe so that any click
or focus event on that iframe (or anything in it) is reported
as a focus/click event on the `<iframe>` itself.

### registerWin
Registers listeners on the specified window (either the main
window or an iframe's window) to detect when the user has clicked somewhere
or focused somewhere.

### unregisterIframe
Unregisters listeners on the specified iframe created by registerIframe.
After calling be sure to delete or null out the handle itself.

### unregisterWin
Unregisters listeners on the specified window (either the main
window or an iframe's window) according to handle returned from registerWin().
After calling be sure to delete or null out the handle itself.

