# Module: dojo/dnd/AutoSource

*Constructor*

# Constructor

## Summary

a source that syncs its DnD nodes by default
## Properties

### accept


### allowNested
Indicates whether to allow dnd item nodes to be nested within other elements.
By default this is false, indicating that only direct children of the container can
be draggable dnd item nodes

### autoSync


### copyOnly


### current
The DOM node the mouse is currently hovered over

### declaredClass


### delay


### generateText


### horizontal


### isSource


### map
Map from an item's id (which is also the DOMNode's id) to
the dojo/dnd/Container.Item itself.

### selection
The set of id's that are currently selected, such that this.selection[id] == 1
if the node w/that id is selected.  Can iterate over selected node's id's like:

        for(var id in this.selection)

### selfAccept


### selfCopy


### singular


### skipForm


### withHandles


## Methods

### checkAcceptance
checks if the target can accept nodes from this source

### clearItems
removes all data items from the map

### copyState
Returns true if we need to copy items, false to move.
It is separated to be overwritten dynamically, if needed.

### creator
creator function, dummy at the moment

### delItem
removes a data item from the map by its key (id)

### deleteSelectedNodes
deletes all selected items

### destroy
prepares the object to be garbage-collected

### emit


### forInItems
iterates over a data map skipping members that
are present in the empty object (IE and/or 3rd-party libraries).

### forInSelectedItems
iterates over selected items;
see `dojo/dnd/Container.forInItems()` for details

### getAllNodes
returns a list (an array) of all valid child nodes

### getItem
returns a data item by its key (id)

### getSelectedNodes
returns a list (an array) of selected nodes

### insertNodes
inserts new data items (see `dojo/dnd/Container.insertNodes()` method for details)

### markupFactory


### on


### onDndCancel
topic event processor for /dnd/cancel, called to cancel the DnD operation

### onDndDrop
topic event processor for /dnd/drop, called to finish the DnD operation

### onDndSourceOver
topic event processor for /dnd/source/over, called when detected a current source

### onDndStart
topic event processor for /dnd/start, called to initiate the DnD operation

### onDraggingOut
called during the active DnD operation, when items
are dragged away from this target, and it is not disabled

### onDraggingOver
called during the active DnD operation, when items
are dragged over this target, and it is not disabled

### onDrop
called only on the current target, when drop is performed

### onDropExternal
called only on the current target, when drop is performed
from an external source

### onDropInternal
called only on the current target, when drop is performed
from the same target/source

### onMouseDown
event processor for onmousedown

### onMouseMove
event processor for onmousemove

### onMouseOut
event processor for onmouseout

### onMouseOver
event processor for onmouseover or touch, to mark that element as the current element

### onMouseUp
event processor for onmouseup

### onOutEvent
this function is called once, when mouse is out of our container

### onOverEvent
this function is called once, when mouse is over our container

### onSelectStart
event processor for onselectevent and ondragevent

### selectAll
selects all items

### selectNone
unselects all items

### setItem
associates a data item with its key (id)

### startup
collects valid child items and populate the map

### sync
sync up the node list with the data map

