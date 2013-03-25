# Module: dijit/_Container

*Constructor*

# Constructor

## Summary

Mixin for widgets that contain HTML and/or a set of widget children.
## Properties

### declaredClass


## Methods

### addChild
Makes the given widget a child of this widget.

### buildRendering


### getIndexOfChild
Gets the index of the child in this container or -1 if not found

### hasChildren
Returns true if widget has child widgets, i.e. if this.containerNode contains widgets.

### removeChild
Removes the passed widget instance from this widget but does
not destroy it.  You can also pass in an integer indicating
the index within the container to remove (ie, removeChild(5) removes the sixth widget).

