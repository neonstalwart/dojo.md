# Module: dijit/tree/dndSource

*Constructor*

# Constructor

## Summary

Handles drag and drop operations (as a source or a target) for `dijit.Tree`
## Properties

### accept
List of accepted types (text strings) for the Tree; defaults to
["text"]

### betweenThreshold
Distance from upper/lower edge of node to allow drop to reorder nodes

### copyOnly
Copy items, if true, use a state of Ctrl key otherwise

### current
The currently hovered TreeNode.  Not set to anything for keyboard operation.  (TODO: change?)

### declaredClass


### dragThreshold
The move delay in pixels before detecting a drag; 5 by default

### generateText


### isSource
Can be used as a DnD source.

### selection
(id to DomNode) map for every TreeNode that's currently selected.
The DOMNode is the TreeNode.rowNode.

### singular
Allows selection of only one element, if true.
Tree hasn't been tested in singular=true mode, unclear if it works.

## Methods

### addTreeNode
add node to current selection

### checkAcceptance
Checks if the target can accept nodes from this source

### checkItemAcceptance
Stub function to be overridden if one wants to check for the ability to drop at the node/item level

### copyState
Returns true, if we need to copy items, false to move.
It is separated to be overwritten dynamically, if needed.

### destroy
Prepares the object to be garbage-collected.

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

### itemCreator
Returns objects passed to `Tree.model.newItem()` based on DnD nodes
dropped onto the tree.   Developer must override this method to enable
dropping from external sources onto this Tree, unless the Tree.model's items
happen to look like {id: 123, name: "Apple" } with no other attributes.

### onClickPress
Event processor for onmousedown/ontouchstart/onkeydown corresponding to a click event

### onClickRelease
Event processor for onmouseup/ontouchend/onkeyup corresponding to a click event

### onDndCancel
Topic event processor for /dnd/cancel, called to cancel the DnD operation

### onDndDrop
Topic event processor for /dnd/drop, called to finish the DnD operation.

### onDndSourceOver
Topic event processor for /dnd/source/over, called when detected a current source.

### onDndStart
Topic event processor for /dnd/start, called to initiate the DnD operation

### onMouseDown
Event processor for onmousedown/ontouchstart

### onMouseMove
Called for any onmousemove/ontouchmove events over the Tree

### onMouseOut
Event processor for when mouse is moved away from a TreeNode

### onMouseOver
Called when mouse is moved over a TreeNode

### onMouseUp
Event processor for onmouseup/ontouchend

### onOutEvent
This method is called when mouse is moved out of our container (like onmouseleave)

### onOverEvent
This method is called when mouse is moved over our container (like onmouseenter)

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

