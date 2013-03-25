# Module: dijit/tree/ObjectStoreModel

*Constructor*

# Constructor

## Summary

Implements dijit/tree/model connecting dijit/Tree to a dojo/store/api/Store that implements
getChildren().

If getChildren() returns an array with an observe() method, then it will be leveraged to reflect
store updates to the tree.   So, this class will work best when:

1. the store implements dojo/store/Observable
2. getChildren() is implemented as a query to the server (i.e. it calls store.query())

Drag and Drop: To support drag and drop, besides implementing getChildren()
and dojo/store/Observable, the store must support the parent option to put().
And in order to have child elements ordered according to how the user dropped them,
put() must support the before option.
## Properties

### declaredClass


### labelAttr
Get label for tree node from this attribute

### query
Specifies datastore query to return the root item for the tree.
Must only return a single item.   Alternately can just pass in pointer
to root item.

### root
Pointer to the root item from the dojo/store/api/Store (read only, not a parameter)

### store
Underlying store

## Methods

### destroy


### getChildren
Calls onComplete() with array of child items of given parent item.

### getIdentity


### getLabel
Get the label for an item

### getRoot
Calls onItem with the root item for the tree, possibly a fabricated item.
Calls onError on error.

### isItem


### mayHaveChildren
Tells if an item has or may have children.  Implementing logic here
avoids showing +/- expando icon for nodes that we know don't have children.
(For efficiency reasons we may not want to check if an element actually
has children until user clicks the expando node).

Application code should override this method based on the data, for example
it could be `return item.leaf == true;`.

### newItem
Creates a new item.   See `dojo/data/api/Write` for details on args.
Used in drag & drop when item from external source dropped onto tree.

### onChange
Callback whenever an item has changed, so that Tree
can update the label, icon, etc.   Note that changes
to an item's children or parent(s) will trigger an
onChildrenChange() so you can ignore those changes here.

### onChildrenChange
Callback to do notifications about new, updated, or deleted items.

### onDelete
Callback when an item has been deleted.
Actually we have no way of knowing this with the new dojo.store API,
so this method is never called (but it's left here since Tree connects
to it).

### pasteItem
Move or copy an item from one parent item to another.
Used in drag & drop

