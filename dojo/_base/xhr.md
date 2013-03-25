# Module: dojo/_base/xhr

## Summary

Deprecated.   Use dojo/request instead.
## Description

Sends an HTTP request with the given method.
See also dojo.xhrGet(), xhrPost(), xhrPut() and dojo.xhrDelete() for shortcuts
for those HTTP methods. There are also methods for "raw" PUT and POST methods
via dojo.rawXhrPut() and dojo.rawXhrPost() respectively.
## Properties

### contentHandlers
A map of available XHR transport handle types. Name matches the
`handleAs` attribute passed to XHR calls.

## Methods

### _getText


### _ioAddQueryToUrl
Adds query params discovered by the io deferred construction to the URL.
Only use this for operations which are fundamentally GET-type operations.

### _ioCancelAll
Cancels all pending IO requests, regardless of IO type
(xhr, script, iframe).

### _ioNotifyStart
If dojo.publish is available, publish topics
about the start of a request queue and/or the
the beginning of request.

Used by IO transports. An IO transport should
call this method before making the network connection.

### _ioSetArgs
sets up the Deferred and ioArgs property on the Deferred so it
can be used in an io call.

### _ioWatch
Watches the io request represented by dfd to see if it completes.

### _isDocumentOk


### _xhrObj
does the work of portably generating a new XMLHTTPRequest object.

### del
Sends an HTTP DELETE request to the server.

### fieldToObject
Serialize a form field to a JavaScript object.

### formToJson
Create a serialized JSON string from a form node or string
ID identifying the form to serialize

### formToObject
Serialize a form node to a JavaScript object.

### formToQuery
Returns a URL-encoded string representing the form passed as either a
node or string ID identifying the form to serialize

### get
Sends an HTTP GET request to the server.

### objectToQuery
takes a name/value mapping object and returns a string representing
a URL-encoded version of that object.

### post
Sends an HTTP POST request to the server. In addition to the properties
listed for the dojo.__XhrArgs type, the following property is allowed:

### put
Sends an HTTP PUT request to the server. In addition to the properties
listed for the dojo.__XhrArgs type, the following property is allowed:

### queryToObject
Create an object representing a de-serialized query section of a
URL. Query keys with multiple values are returned in an array.


# Constructor

