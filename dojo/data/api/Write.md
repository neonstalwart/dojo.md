# Module: dojo/data/api/Write

*Constructor*

# Constructor

## Summary

This is an abstract API that data provider implementations conform to.
This file defines function signatures and intentionally leaves all the
functions unimplemented.
## Properties

### declaredClass


## Methods

### close
The close() method is intended for instructing the store to 'close' out
any information associated with a particular request.

### containsValue
Returns true if the given *value* is one of the values that getValues()
would return.

### deleteItem
Deletes an item from the store.

### fetch
Given a query and set of defined options, such as a start and count of items to return,
this method executes the query and makes the results available as data items.
The format and expectations of stores is that they operate in a generally asynchronous
manner, therefore callbacks are always used to return items located by the fetch parameters.

### getAttributes
Returns an array with all the attributes that this item has.  This
method will always return an array; if the item has no attributes
at all, getAttributes() will return an empty array: [].

### getFeatures
See dojo/data/api/Read.getFeatures()

### getLabel
Method to inspect the item and return a user-readable 'label' for the item
that provides a general/adequate description of what the item is.

### getLabelAttributes
Method to inspect the item and return an array of what attributes of the item were used
to generate its label, if any.

### getValue
Returns a single attribute value.
Returns defaultValue if and only if *item* does not have a value for *attribute*.
Returns null if and only if null was explicitly set as the attribute value.
Returns undefined if and only if the item does not have a value for the
given attribute (which is the same as saying the item does not have the attribute).

### getValues
This getValues() method works just like the getValue() method, but getValues()
always returns an array rather than a single attribute value.  The array
may be empty, may contain a single attribute value, or may contain
many attribute values.
If the item does not have a value for the given attribute, then getValues()
will return an empty array: [].  (So, if store.hasAttribute(item, attribute)
has a return of false, then store.getValues(item, attribute) will return [].)

### hasAttribute
Returns true if the given *item* has a value for the given *attribute*.

### isDirty
Given an item, isDirty() returns true if the item has been modified
since the last save().  If isDirty() is called with no *item* argument,
then this function returns true if any item has been modified since
the last save().

### isItem
Returns true if *something* is an item and came from the store instance.
Returns false if *something* is a literal, an item from another store instance,
or is any object other than an item.

### isItemLoaded
Returns false if isItem(something) is false.  Returns false if
if isItem(something) is true but the the item is not yet loaded
in local memory (for example, if the item has not yet been read
from the server).

### loadItem
Given an item, this method loads the item so that a subsequent call
to store.isItemLoaded(item) will return true.  If a call to
isItemLoaded() returns true before loadItem() is even called,
then loadItem() need not do any work at all and will not even invoke
the callback handlers.  So, before invoking this method, check that
the item has not already been loaded.

### newItem
Returns a newly created item.  Sets the attributes of the new
item based on the *keywordArgs* provided.  In general, the attribute
names in the keywords become the attributes in the new item and as for
the attribute values in keywordArgs, they become the values of the attributes
in the new item.  In addition, for stores that support hierarchical item
creation, an optional second parameter is accepted that defines what item is the parent
of the new item and what attribute of that item should the new item be assigned to.
In general, this will assume that the attribute targeted is multi-valued and a new item
is appended onto the list of values for that attribute.

### revert
Discards any unsaved changes.

### save
Saves to the server all the changes that have been made locally.
The save operation may take some time and is generally performed
in an asynchronous fashion.  The outcome of the save action is
is passed into the set of supported callbacks for the save.

### setValue
Sets the value of an attribute on an item.
Replaces any previous value or values.

### setValues
Adds each value in the *values* array as a value of the given
attribute on the given item.
Replaces any previous value or values.
Calling store.setValues(x, y, []) (with *values* as an empty array) has
the same effect as calling store.unsetAttribute(x, y).

### unsetAttribute
Deletes all the values of an attribute on an item.

