# Module: dojo/rpc/JsonpService

*Constructor*

# Constructor

## Summary

Generic JSONP service.  Minimally extends RpcService to allow
easy definition of nearly any JSONP style service. Example
SMD files exist in dojox.data
## Properties

### declaredClass


### serviceUrl


### strictArgChecks


## Methods

### bind
JSONP bind method. Takes remote method, parameters,
deferred, and a url, calls createRequest to make a JSON-RPC
envelope and passes that off with bind.

### createRequest
create a JSONP req

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

