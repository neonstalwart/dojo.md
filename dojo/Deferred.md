# dojo/Deferred

## Summary

Creates a new deferred. This API is preferred over
`dojo/_base/Deferred`.
## Description

Creates a new deferred, as an abstraction over (primarily)
asynchronous operations. The deferred is the private interface
that should not be returned to calling code. That's what the
`promise` is for. See `dojo/promise/Promise`.
## Static Properties

### promise


## Static Methods

### cancel
Inform the deferred it may cancel its asynchronous operation.

### isCanceled
Checks whether the deferred has been canceled.

### isFulfilled
Checks whether the deferred has been resolved or rejected.

### isRejected
Checks whether the deferred has been rejected.

### isResolved
Checks whether the deferred has been resolved.

### progress
Emit a progress update on the deferred.

### reject
Reject the deferred.

### resolve
Resolve the deferred.

### then
Add new callbacks to the deferred.

## Static Methods

### toString


