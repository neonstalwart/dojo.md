# Module: dojo/promise/Promise

## Summary

The public interface to a deferred.
## Description

The public interface to a deferred. All promises in Dojo are
instances of this class.
# Constructor

## Methods

### always
Add a callback to be invoked when the promise is resolved
or rejected.

### cancel
Inform the deferred it may cancel its asynchronous operation.

### isCanceled
Checks whether the promise has been canceled.

### isFulfilled
Checks whether the promise has been resolved or rejected.

### isRejected
Checks whether the promise has been rejected.

### isResolved
Checks whether the promise has been resolved.

### otherwise
Add new errbacks to the promise.

### then
Add new callbacks to the promise.

### trace
Trace the promise.

### traceRejected
Trace rejection of the promise.

