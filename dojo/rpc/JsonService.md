# Module: dojo/rpc/JsonService

*Constructor*

# Constructor

## Summary

TODOC
## Properties

### bustCache


### contentType


### declaredClass


### lastSubmissionId


### serviceUrl


### strictArgChecks


## Methods

### bind
JSON-RPC bind method. Takes remote method, parameters,
deferred, and a url, calls createRequest to make a JSON-RPC
envelope and passes that off with bind.

### callRemote
call an arbitrary remote method without requiring it to be
predefined with SMD

### createRequest
create a JSON-RPC envelope for the request

### errorCallback
create callback that calls the Deferred errback method

### generateMethod
generate the local bind methods for the remote object

### parseResults
parse the result envelope and pass the results back to
the callback function

### processSmd
callback method for receipt of a smd object.  Parse the smd
and generate functions based on the description

### resultCallback
create callback that calls the Deferred's callback method

