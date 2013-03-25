# Module: dojo/dnd/Manager

*Constructor*

## Methods

### manager
Returns the current DnD manager.  Creates one if it is not created yet.

# Constructor

## Summary

the manager of DnD operations (usually a singleton)
## Properties

### OFFSET_X


### OFFSET_Y


### declaredClass


## Methods

### canDrop
called to notify if the current target can accept items

### emit


### makeAvatar
makes the avatar; it is separate to be overwritten dynamically, if needed

### on


### onKeyDown
event processor for onkeydown:
watching for CTRL for copy/move status, watching for ESCAPE to cancel the drag

### onKeyUp
event processor for onkeyup, watching for CTRL for copy/move status

### onMouseMove
event processor for onmousemove

### onMouseUp
event processor for onmouseup

### outSource
called when a source detected a mouse-out condition

### overSource
called when a source detected a mouse-over condition

### startDrag
called to initiate the DnD operation

### stopDrag
stop the DnD in progress

### updateAvatar
updates the avatar; it is separate to be overwritten dynamically, if needed

