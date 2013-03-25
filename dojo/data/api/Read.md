# dojo/data/api/Read

*Constructor*

## Summary

This is an abstract API that data provider implementations conform to.
This file defines methods signatures and intentionally leaves all the
methods unimplemented.  For more information on the dojo.data APIs,
please visit: http://www.dojotoolkit.org/node/98
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

### getAttributes
Returns an array with all the attributes that this item has.  This
method will always return an array; if the item has no attributes
at all, getAttributes() will return an empty array: [].

### getFeatures
The getFeatures() method returns an simple keyword values object
that specifies what interface features the datastore implements.
A simple CsvStore may be read-only, and the only feature it
implements will be the 'dojo/data/api/Read' interface, so the
getFeatures() method will return an object like this one:
{'dojo.data.api.Read': true}.
A more sophisticated datastore might implement a variety of
interface features, like 'dojo.data.api.Read', 'dojo/data/api/Write',
'dojo.data.api.Identity', and 'dojo/data/api/Attribution'.

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

