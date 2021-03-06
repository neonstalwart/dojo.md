# Module: dojo/dnd/Moveable

*Constructor*

# Constructor

## Summary

an object, which makes a node movable
## Properties

### declaredClass


### delay


### handle


### skip


## Methods

### destroy
stops watching for possible move, deletes all references, so the object can be garbage-collected

### emit


### markupFactory


### on


### onDragDetected
called when the drag is detected;
responsible for creation of the mover

### onFirstMove
called during the very first move notification;
can be used to initialize coordinates, can be overwritten.

### onMouseDown
event processor for onmousedown/ontouchstart, creates a Mover for the node

### onMouseMove
event processor for onmousemove/ontouchmove, used only for delayed drags

### onMouseUp
event processor for onmouseup, used only for delayed drags

### onMove
called during every move notification;
should actually move the node; can be overwritten.

### onMoveStart
called before every move operation

### onMoveStop
called after every move operation

### onMoved
called after every incremental move; can be overwritten.

### onMoving
called before every incremental move; can be overwritten.

### onSelectStart
event processor for onselectevent and ondragevent

