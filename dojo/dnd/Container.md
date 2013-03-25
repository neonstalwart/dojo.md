# Module: dojo/dnd/Container

*Constructor*

## Properties

### __ContainerArgs


## Methods

### Item
Represents (one of) the source node(s) being dragged.
Contains (at least) the "type" and "data" attributes.

# Constructor

## Summary

a Container object, which knows when mouse hovers over it,
and over which element it hovers
## Properties

### allowNested
Indicates whether to allow dnd item nodes to be nested within other elements.
By default this is false, indicating that only direct children of the container can
be draggable dnd item nodes

### current
The DOM node the mouse is currently hovered over

### declaredClass


### map
Map from an item's id (which is also the DOMNode's id) to
the dojo/dnd/Container.Item itself.

### skipForm


## Methods

### _addItemClass
adds a class with prefix "dojoDndItem"

### _changeState
changes a named state to new state value

### _getChildByEvent
gets a child, which is under the mouse at the moment, or null

### _normalizedCreator
adds all necessary data to the output of the user-supplied creator function

### _removeItemClass
removes a class with prefix "dojoDndItem"

### clearItems
removes all data items from the map

### creator
creator function, dummy at the moment

### delItem
removes a data item from the map by its key (id)

### destroy
prepares this object to be garbage-collected

### emit


### forInItems
iterates over a data map skipping members that
are present in the empty object (IE and/or 3rd-party libraries).

### getAllNodes
returns a list (an array) of all valid child nodes

### getItem
returns a data item by its key (id)

### insertNodes
inserts an array of new nodes before/after an anchor node

### markupFactory


### on


### onMouseOut
event processor for onmouseout

### onMouseOver
event processor for onmouseover or touch, to mark that element as the current element

### onOutEvent
this function is called once, when mouse is out of our container

### onOverEvent
this function is called once, when mouse is over our container

### onSelectStart
event processor for onselectevent and ondragevent

### setItem
associates a data item with its key (id)

### startup
collects valid child items and populate the map

### sync
sync up the node list with the data map

