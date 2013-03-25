# Module: dijit/typematic

## Summary

These functions are used to repetitively call a user specified callback
method when a specific key or mouse click over a specific DOM node is
held down for a specific amount of time.
Only 1 such event is allowed to occur on the browser page at 1 time.
## Methods

### addKeyListener
Start listening for a specific typematic key.
See also the trigger method for other parameters.

### addListener
Start listening for a specific typematic key and mouseclick.
This is a thin wrapper to addKeyListener and addMouseListener.
See the addMouseListener and addKeyListener methods for other parameters.

### addMouseListener
Start listening for a typematic mouse click.
See the trigger method for other parameters.

### stop
Stop an ongoing timed, repeating callback sequence.

### trigger
Start a timed, repeating callback sequence.
If already started, the function call is ignored.
This method is not normally called by the user but can be
when the normal listener code is insufficient.

