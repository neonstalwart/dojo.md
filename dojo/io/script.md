# Module: dojo/io/script

## Summary

TODOC
## Properties

### _counter


### _deadScripts


## Methods

### _addDeadScript
sets up an entry in the deadScripts array.

### _canAttach
A method that can be overridden by other modules
to control when the script attachment occurs.

### _deferredCancel
canceller function for xhr._ioSetArgs call.

### _deferredError
errHandler function for xhr._ioSetArgs call.

### _deferredOk
okHandler function for xhr._ioSetArgs call.

### _ioCheck
inflight check function to see if IO finished.

### _jsonpCallback
generic handler for jsonp callback. A pointer to this function
is used for all jsonp callbacks.  NOTE: the "this" in this
function will be the Deferred object that represents the script
request.

### _makeScriptDeferred
sets up a Deferred object for an IO request.

### _resHandle
inflight function to handle a completed response.

### _validCheck
inflight check function to see if dfd is still valid.

### attach
creates a new `<script>` tag pointing to the specified URL and
adds it to the document.

### get
sends a get request using a dynamically created script tag.

### remove
removes the script element with the given id, from the given frameDocument.
If no frameDocument is passed, the current document is used.

# Constructor

## Methods

### hasOwnProperty


### toString


