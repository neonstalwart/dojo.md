# dojo/store/Memory

*Constructor*

## Summary

This is a basic in-memory object store. It implements dojo/store/api/Store.
## Static Properties

### data
The array of all the objects in the memory store

### declaredClass


### idProperty
Indicates the property to use as the identity property. The values of this
property should be unique.

### index
An index of data indices into the data array by id

## Static Methods

### add
Creates an object, throws an error if the object already exists

### get
Retrieves an object by its identity

### getChildren
Retrieves the children of an object.

### getIdentity
Returns an object's identity

### getMetadata
Returns any metadata about the object. This may include attribution,
cache directives, history, or version information.

### put
Stores an object

### query
Queries the store for objects.

### queryEngine
Defines the query engine to use for querying the data store

### remove
Deletes an object by its identity

### setData
Sets the given data as the source for this store, and indexes it

### transaction
Starts a new transaction.
Note that a store user might not call transaction() prior to using put,
delete, etc. in which case these operations effectively could be thought of
as "auto-commit" style actions.

