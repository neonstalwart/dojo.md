# Module: dojo/rpc/RpcService

*Constructor*

# Constructor

## Summary

TODOC
## Properties

### declaredClass


### serviceUrl


### strictArgChecks


## Methods

### errorCallback
create callback that calls the Deferred errback method

### generateMethod
generate the local bind methods for the remote object

### parseResults
parse the results coming back from an rpc request.  this
base implementation, just returns the full object
subclasses should parse and only return the actual results

### processSmd
callback method for receipt of a smd object.  Parse the smd
and generate functions based on the description

### resultCallback
create callback that calls the Deferred's callback method

