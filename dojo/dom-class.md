# Module: dojo/dom-class

## Summary

This module defines the core dojo DOM class API.
## Methods

### add
Adds the specified classes to the end of the class list on the
passed node. Will not re-apply duplicate classes.


### contains
Returns whether or not the specified classes are a portion of the
class list currently applied to the node.

### remove
Removes the specified classes from node. No `contains()`
check is required.


### replace
Replaces one or more classes on a node if not present.
Operates more quickly than calling dojo.removeClass and dojo.addClass


### toggle
Adds a class to node if not present, or removes if present.
Pass a boolean condition if you want to explicitly add or remove.
Returns the condition that was specified directly or indirectly.


# Constructor

## Methods

### hasOwnProperty


