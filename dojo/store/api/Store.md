# Module: dojo/store/api/Store

*Constructor*

## Properties

### PutDirectives


### QueryOptions


### QueryResults


### SortInformation


### Transaction


# Constructor

## Summary

This is an abstract API that data provider implementations conform to.
This file defines methods signatures and intentionally leaves all the
methods unimplemented.  For more information on the ,
please visit: http://dojotoolkit.org/reference-guide/dojo/store.html
Every method and property is optional, and is only needed if the functionality
it provides is required.
Every method may return a promise for the specified return value if the
execution of the operation is asynchronous (except
for query() which already defines an async return value).
## Properties

### idProperty
If the store has a single primary key, this indicates the property to use as the
identity property. The values of this property should be unique.

### queryEngine
If the store can be queried locally (on the client side in JS), this defines
the query engine to use for querying the data store.
This takes a query and query options and returns a function that can execute
the provided query on a JavaScript array. The queryEngine may be replace to
provide more sophisticated querying capabilities. For example:

    var query = store.queryEngine({foo:"bar"}, {count:10});
    query(someArray) -> filtered array

The returned query function may have a "matches" property that can be
used to determine if an object matches the query. For example:

    query.matches({id:"some-object", foo:"bar"}) -> true
    query.matches({id:"some-object", foo:"something else"}) -> false

## Methods

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
Queries the store for objects. This does not alter the store, but returns a
set of data from the store.

### remove
Deletes an object by its identity

### transaction
Starts a new transaction.
Note that a store user might not call transaction() prior to using put,
delete, etc. in which case these operations effectively could be thought of
as "auto-commit" style actions.

