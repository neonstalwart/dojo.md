# Module: dojo/store/JsonRest

*Constructor*

# Constructor

## Summary

This is a basic store for RESTful communicating with a server through JSON
formatted data. It implements dojo/store/api/Store.
## Properties

### accepts
Defines the Accept header to use on HTTP requests

### ascendingPrefix
The prefix to apply to sort attribute names that are ascending

### declaredClass


### descendingPrefix
The prefix to apply to sort attribute names that are ascending

### headers
Additional headers to pass in all requests to the server. These can be overridden
by passing additional headers to calls to the store.

### idProperty
Indicates the property to use as the identity property. The values of this
property should be unique.

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

### target
The target base URL to use for all requests to the server. This string will be
prepended to the id to generate the URL (relative or absolute) for requests
sent to the server

## Methods

### add
Adds an object. This will trigger a PUT request to the server
if the object has an id, otherwise it will trigger a POST request.

### get
Retrieves an object by its identity. This will trigger a GET request to the server using
the url `this.target + id`.

### getChildren
Retrieves the children of an object.

### getIdentity
Returns an object's identity

### getMetadata
Returns any metadata about the object. This may include attribution,
cache directives, history, or version information.

### put
Stores an object. This will trigger a PUT request to the server
if the object has an id, otherwise it will trigger a POST request.

### query
Queries the store for objects. This will trigger a GET request to the server, with the
query added as a query string.

### remove
Deletes an object by its identity. This will trigger a DELETE request to the server.

### transaction
Starts a new transaction.
Note that a store user might not call transaction() prior to using put,
delete, etc. in which case these operations effectively could be thought of
as "auto-commit" style actions.

