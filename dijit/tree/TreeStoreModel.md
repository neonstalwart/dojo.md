# Module: dijit/tree/TreeStoreModel

*Constructor*

# Constructor

## Summary

Implements dijit/Tree/model connecting to a dojo.data store with a single
root item.  Any methods passed into the constructor will override
the ones defined here.
## Properties

### childrenAttrs
One or more attribute names (attributes in the dojo.data item) that specify that item's children

### declaredClass


### deferItemLoadingUntilExpand
Setting this to true will cause the TreeStoreModel to defer calling loadItem on nodes
until they are expanded. This allows for lazying loading where only one
loadItem (and generally one network call, consequently) per expansion
(rather than one for each child).
This relies on partial loading of the children items; each children item of a
fully loaded item should contain the label and info about having children.

### labelAttr
If specified, get label for tree node from this attribute, rather
than by calling store.getLabel()

### newItemIdAttr
Name of attribute in the Object passed to newItem() that specifies the id.

If newItemIdAttr is set then it's used when newItem() is called to see if an
item with the same id already exists, and if so just links to the old item
(so that the old item ends up with two parents).

Setting this to null or "" will make every drop create a new item.

### query
Specifies datastore query to return the root item for the tree.
Must only return a single item.   Alternately can just pass in pointer
to root item.

### root
Pointer to the root item (read only, not a parameter)

### store
Underlying store

## Methods

### destroy


### fetchItemByIdentity
Given the identity of an item, this method returns the item that has
that identity through the onItem callback.  Conforming implementations
should return null if there is no item with the given identity.
Implementations of fetchItemByIdentity() may sometimes return an item
from a local cache and may sometimes fetch an item from a remote server.

### getChildren
Calls onComplete() with array of child items of given parent item, all loaded.

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
has children until user clicks the expando node)

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

### onDeleteItem
Handler for delete notifications from underlying store

### onNewItem
Handler for when new items appear in the store, either from a drop operation
or some other way.   Updates the tree view (if necessary).

### onSetItem
Updates the tree view according to changes in the data store.

### pasteItem
Move or copy an item from one parent item to another.
Used in drag & drop

