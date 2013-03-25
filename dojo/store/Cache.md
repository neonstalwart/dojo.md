# Module: dojo/store/Cache

*Constructor*

# Constructor

## Summary

The Cache store wrapper takes a master store and a caching store,
caches data from the master into the caching store for faster
lookup. Normally one would use a memory store for the caching
store and a server store like JsonRest for the master store.
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
Add the given object to the store.

### evict
Remove the object with the given id from the underlying caching store.

### get
Get the object with the specific id.

### getChildren
Retrieves the children of an object.

### getIdentity
Returns an object's identity

### getMetadata
Returns any metadata about the object. This may include attribution,
cache directives, history, or version information.

### put
Put the object into the store (similar to an HTTP PUT).

### query
Query the underlying master store and cache any results.

### remove
Remove the object with the specific id.

### transaction
Starts a new transaction.
Note that a store user might not call transaction() prior to using put,
delete, etc. in which case these operations effectively could be thought of
as "auto-commit" style actions.

