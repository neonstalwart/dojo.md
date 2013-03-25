# Module: dijit/tree/ForestStoreModel

*Constructor*

# Constructor

## Summary

Interface between a dijit.Tree and a dojo.data store that doesn't have a root item,
a.k.a. a store that has multiple "top level" items.

## Description

Use this class to wrap a dojo.data store, making all the items matching the specified query
appear as children of a fabricated "root item".  If no query is specified then all the
items returned by fetch() on the underlying store become children of the root item.
This class allows dijit.Tree to assume a single root item, even if the store doesn't have one.

When using this class the developer must override a number of methods according to their app and
data, including:

- onNewRootItem
- onAddToRoot
- onLeaveRoot
- onNewItem
- onSetItem
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
Specifies the set of children of the root item.

### root
Pointer to the root item (read only, not a parameter)

### rootId
ID of fabricated root item

### rootLabel
Label of fabricated root item

### store
Underlying store

## Methods

### destroy


### fetchItemByIdentity


### getChildren
Calls onComplete() with array of child items of given parent item, all loaded.

### getIdentity


### getLabel


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
Creates a new item.   See dojo/data/api/Write for details on args.
Used in drag & drop when item from external source dropped onto tree.

### onAddToRoot
Called when item added to root of tree; user must override this method
to modify the item so that it matches the query for top level items

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

### onLeaveRoot
Called when item removed from root of tree; user must override this method
to modify the item so it doesn't match the query for top level items

### onNewItem
Handler for when new items appear in the store.  Developers should override this
method to be more efficient based on their app/data.

### onNewRootItem
User can override this method to modify a new element that's being
added to the root of the tree, for example to add a flag like root=true

### onSetItem
Updates the tree view according to changes to an item in the data store.
Developers should override this method to be more efficient based on their app/data.

### pasteItem
Move or copy an item from one parent item to another.
Used in drag & drop

