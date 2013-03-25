# Module: dojo/data/ObjectStore

*Constructor*

# Constructor

## Summary

A Dojo Data implementation that wraps Dojo object stores for backwards
compatibility.
## Properties

### declaredClass


### labelProperty


### objectStore


## Methods

### changing
adds an object to the list of dirty objects.  This object
contains a reference to the object itself as well as a
cloned and trimmed version of old object for use with
revert.

### close
See dojo/data/api/Read.close()

### containsValue
Checks to see if 'item' has 'value' at 'attribute'

### deleteItem
deletes item and any references to that item from the store.

### emit


### fetch
See dojo/data/api/Read.fetch()

### fetchItemByIdentity
fetch an item by its identity, by looking in our index of what we have loaded

### getAttributes
Gets the available attributes of an item's 'property' and returns
it as an array.

### getFeatures
return the store feature set

### getIdentity
returns the identity of the given item
See dojo/data/api/Read.getIdentity()

### getIdentityAttributes
returns the attributes which are used to make up the
identity of an item.  Basically returns this.objectStore.idProperty
See dojo/data/api/Read.getIdentityAttributes()

### getLabel
See dojo/data/api/Read.getLabel()

### getLabelAttributes
See dojo/data/api/Read.getLabelAttributes()

### getValue
Gets the value of an item's 'property'

### getValues
Gets the value of an item's 'property' and returns
it. If this value is an array it is just returned,
if not, the value is added to an array and that is returned.

### hasAttribute
Checks to see if item has attribute

### isDirty
returns true if the item is marked as dirty or true if there are any dirty items

### isItem
Checks to see if the argument is an item

### isItemLoaded
Checks to see if the item is loaded.

### loadItem
Loads an item and calls the callback handler. Note, that this will call the callback
handler even if the item is loaded. Consequently, you can use loadItem to ensure
that an item is loaded is situations when the item may or may not be loaded yet.
If you access a value directly through property access, you can use this to load
a lazy value as well (doesn't need to be an item).

### newItem
adds a new item to the store at the specified point.
Takes two parameters, data, and options.

### on


### onDelete
See dojo/data/api/Notification.onDelete()

### onFetch
Called when a fetch occurs

### onNew
See dojo/data/api/Notification.onNew()

### onSet
See dojo/data/api/Notification.onSet()

### revert
returns any modified data to its original state prior to a save();

### save
Saves the dirty data using object store provider. See dojo/data/api/Write for API.

### setValue
sets 'attribute' on 'item' to 'value'
See dojo/data/api/Write.setValue()

### setValues
sets 'attribute' on 'item' to 'value' value
must be an array.
See dojo/data/api/Write.setValues()

### unsetAttribute
unsets 'attribute' on 'item'
See dojo/data/api/Write.unsetAttribute()

