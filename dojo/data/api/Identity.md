# dojo/data/api/Identity

*Constructor*

## Summary

This is an abstract API that data provider implementations conform to.
This file defines methods signatures and intentionally leaves all the
methods unimplemented.
## Static Properties

### declaredClass


## Static Methods

### close
The close() method is intended for instructing the store to 'close' out
any information associated with a particular request.

### containsValue
Returns true if the given *value* is one of the values that getValues()
would return.

### fetch
Given a query and set of defined options, such as a start and count of items to return,
this method executes the query and makes the results available as data items.
The format and expectations of stores is that they operate in a generally asynchronous
manner, therefore callbacks are always used to return items located by the fetch parameters.

### fetchItemByIdentity
Given the identity of an item, this method returns the item that has
that identity through the onItem callback.  Conforming implementations
should return null if there is no item with the given identity.
Implementations of fetchItemByIdentity() may sometimes return an item
from a local cache and may sometimes fetch an item from a remote server,

### getAttributes
Returns an array with all the attributes that this item has.  This
method will always return an array; if the item has no attributes
at all, getAttributes() will return an empty array: [].

### getFeatures
See dojo/data/api/Read.getFeatures()

### getIdentity
Returns a unique identifier for an item.  The return value will be
either a string or something that has a toString() method (such as,
for example, a dojox/uuid object).

### getIdentityAttributes
Returns an array of attribute names that are used to generate the identity.
For most stores, this is a single attribute, but for some complex stores
such as RDB backed stores that use compound (multi-attribute) identifiers
it can be more than one.  If the identity is not composed of attributes
on the item, it will return null.  This function is intended to identify
the attributes that comprise the identity so that so that during a render
of all attributes, the UI can hide the the identity information if it
chooses.

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

