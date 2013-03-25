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


