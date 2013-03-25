# dojo/dnd/autoscroll

## Summary

Used by dojo/dnd/Manager to scroll document or internal node when the user
drags near the edge of the viewport or a scrollable node
## Static Properties

### H_AUTOSCROLL_VALUE


### H_TRIGGER_AUTOSCROLL


### V_AUTOSCROLL_VALUE


### V_TRIGGER_AUTOSCROLL


### _validNodes


### _validOverflow


## Static Methods

### autoScroll
a handler for mousemove and touchmove events, which scrolls the window, if
necessary

### autoScrollNodes
a handler for mousemove and touchmove events, which scrolls the first available
Dom element, it falls back to exports.autoScroll()

### autoScrollStart
Called at the start of a drag.

### getViewport
Returns the dimensions and scroll position of the viewable area of a browser window

## Static Methods

### hasOwnProperty


### toString


