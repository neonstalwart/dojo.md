# Module: dijit/tree/_dndSelector

*Constructor*

# Constructor

**,*protected*

## Summary

This is a base class for `dijit/tree/dndSource`, and isn't meant to be used directly.
It's based on `dojo/dnd/Selector`.
## Properties

### current
The currently hovered TreeNode.  Not set to anything for keyboard operation.  (TODO: change?)

### declaredClass


### selection
(id to DomNode) map for every TreeNode that's currently selected.
The DOMNode is the TreeNode.rowNode.

### singular
Allows selection of only one element, if true.
Tree hasn't been tested in singular=true mode, unclear if it works.

## Methods

### addTreeNode
add node to current selection

### destroy
Prepares the object to be garbage-collected

### forInSelectedItems
Iterates over selected items;
see `dojo/dnd/Container.forInItems()` for details

### getItem
Returns the dojo/dnd/Container._Item (representing a dragged node) by it's key (id).
Called by dojo/dnd/Source.checkAcceptance().

### getSelectedTreeNodes
Returns a list of selected node(s).
Used by dndSource on the start of a drag.

### isTreeNodeSelected
return true if node is currently selected

### onClickPress
Event processor for onmousedown/ontouchstart/onkeydown corresponding to a click event

### onClickRelease
Event processor for onmouseup/ontouchend/onkeyup corresponding to a click event

### onMouseDown
Event processor for onmousedown/ontouchstart

### onMouseMove
event processor for onmousemove/ontouchmove

### onMouseOut
Called when mouse is moved away from a TreeNode

### onMouseOver
Called when mouse is moved over a TreeNode

### onMouseUp
Event processor for onmouseup/ontouchend

### onOutEvent
This function is called once, when mouse is out of our container

### onOverEvent
This function is called once, when mouse is over our container

### removeTreeNode
remove node and it's descendants from current selection

### selectNone
Unselects all items

### setSelection
set the list of selected nodes to be exactly newSelection. All changes to the
selection should be passed through this function, which ensures that derived
attributes are kept up to date. Anchor will be deleted if it has been removed
from the selection, but no new anchor will be added by this function.

### userSelect
Add or remove the given node from selection, responding
to a user action such as a click or keypress.

