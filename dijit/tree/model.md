# Module: dijit/tree/model

*Constructor*

# Constructor

## Summary

Contract for any data provider object for the tree.
## Description

Tree passes in values to the constructor to specify the callbacks.
"item" is typically a dojo/data/Item but it's just a black box so
it could be anything.

This (like `dojo/data/api/Read`) is just documentation, and not meant to be used.
## Properties

### declaredClass


## Methods

### destroy
Destroys this object, releasing connections to the store

### getChildren
Calls onComplete() with array of child items of given parent item, all loaded.
Throws exception on error.

### getIdentity
Returns identity for an item

### getLabel
Get the label for an item

### getRoot
Calls onItem with the root item for the tree, possibly a fabricated item.
Throws exception on error.

### isItem
Returns true if *something* is an item and came from this model instance.
Returns false if *something* is a literal, an item from another model instance,
or is any object other than an item.

### mayHaveChildren
Tells if an item has or may have children.  Implementing logic here
avoids showing +/- expando icon for nodes that we know don't have children.
(For efficiency reasons we may not want to check if an element actually
has children until user clicks the expando node)

### newItem
Creates a new item.   See `dojo/data/api/Write` for details on args.

### onChange
Callback whenever an item has changed, so that Tree
can update the label, icon, etc.   Note that changes
to an item's children or parent(s) will trigger an
onChildrenChange() so you can ignore those changes here.

### onChildrenChange
Callback to do notifications about new, updated, or deleted items.

### pasteItem
Move or copy an item from one parent item to another.
Used in drag & drop.
If oldParentItem is specified and bCopy is false, childItem is removed from oldParentItem.
If newParentItem is specified, childItem is attached to newParentItem.

