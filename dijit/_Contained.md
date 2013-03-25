# Module: dijit/_Contained

*Constructor*

# Constructor

## Summary

Mixin for widgets that are children of a container widget

## Properties

### declaredClass


## Methods

### getIndexInParent
Returns the index of this widget within its container parent.
It returns -1 if the parent does not exist, or if the parent
is not a dijit._Container

### getNextSibling
Returns null if this is the last child of the parent,
otherwise returns the next element sibling to the "right".

### getPreviousSibling
Returns null if this is the first child of the parent,
otherwise returns the next element sibling to the "left".

