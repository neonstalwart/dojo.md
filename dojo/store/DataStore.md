# dojo/store/DataStore

*Constructor*

## Summary

This is an adapter for using Dojo Data stores with an object store consumer.
You can provide a Dojo data store and use this adapter to interact with it through
the Dojo object store API
## Static Properties

### declaredClass


### idProperty
The object property to use to store the identity of the store items.

### store
The object store to convert to a data store

### target


## Static Methods

### _objectConverter


### add
Creates an object, throws an error if the object already exists

### get
Retrieves an object by it's identity. This will trigger a fetchItemByIdentity

### getChildren
Retrieves the children of an object.

### getIdentity
Fetch the identity for the given object.

### getMetadata
Returns any metadata about the object. This may include attribution,
cache directives, history, or version information.

### put
Stores an object by its identity.

### query
Queries the store for objects.

### queryEngine
Defines the query engine to use for querying the data store

### remove
Deletes an object by its identity.

### transaction
Starts a new transaction.
Note that a store user might not call transaction() prior to using put,
delete, etc. in which case these operations effectively could be thought of
as "auto-commit" style actions.

