# dojo/dnd/Mover

*Constructor*

## Summary

an object which makes a node follow the mouse, or touch-drag on touch devices.
Used as a default mover, and as a base class for custom movers.
## Static Properties

### declaredClass


## Static Methods

### destroy
stops the move, deletes all references, so the object can be garbage-collected

### emit


### on


### onFirstMove
makes the node absolute; it is meant to be called only once.
relative and absolutely positioned nodes are assumed to use pixel units

### onMouseMove
event processor for onmousemove/ontouchmove

### onMouseUp


