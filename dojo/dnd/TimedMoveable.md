# dojo/dnd/TimedMoveable

*Constructor*

## Summary

A specialized version of Moveable to support an FPS throttling.
This class puts an upper restriction on FPS, which may reduce
the CPU load. The additional parameter "timeout" regulates
the delay before actually moving the moveable object.
## Static Properties

### declaredClass


### delay


### handle


### skip


### timeout


## Static Methods

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


### onMoveStart
called before every move operation

### onMoveStop


### onMoved
called after every incremental move; can be overwritten.

### onMoving
called before every incremental move; can be overwritten.

### onSelectStart
event processor for onselectevent and ondragevent

