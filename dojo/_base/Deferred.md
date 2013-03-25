# dojo/_base/Deferred

## Summary

Deprecated.   This module defines the legacy dojo/_base/Deferred API.
New code should use dojo/Deferred instead.
## Description

The Deferred API is based on the concept of promises that provide a
generic interface into the eventual completion of an asynchronous action.
The motivation for promises fundamentally is about creating a
separation of concerns that allows one to achieve the same type of
call patterns and logical data flow in asynchronous code as can be
achieved in synchronous code. Promises allows one
to be able to call a function purely with arguments needed for
execution, without conflating the call with concerns of whether it is
sync or async. One shouldn't need to alter a call's arguments if the
implementation switches from sync to async (or vice versa). By having
async functions return promises, the concerns of making the call are
separated from the concerns of asynchronous interaction (which are
handled by the promise).

The Deferred is a type of promise that provides methods for fulfilling the
promise with a successful result or an error. The most important method for
working with Dojo's promises is the then() method, which follows the
CommonJS proposed promise API. An example of using a Dojo promise:


    var resultingPromise = someAsyncOperation.then(function(result){
    ... handle result ...
    },
    function(error){
    ... handle error ...
    });


The .then() call returns a new promise that represents the result of the
execution of the callback. The callbacks will never affect the original promises value.

The Deferred instances also provide the following functions for backwards compatibility:

- addCallback(handler)
- addErrback(handler)
- callback(result)
- errback(result)

Callbacks are allowed to return promises themselves, so
you can build complicated sequences of events with ease.

The creator of the Deferred may specify a canceller.  The canceller
is a function that will be called if Deferred.cancel is called
before the Deferred fires. You can use this to implement clean
aborting of an XMLHttpRequest, etc. Note that cancel will fire the
deferred with a CancelledError (unless your canceller returns
another kind of error), so the errbacks should be prepared to
handle that error for cancellable Deferreds.
## Static Properties

### promise


## Static Methods

### addCallbacks
Adds callback and error callback for this deferred instance.

### callback
Fulfills the Deferred instance successfully with the provide value

### cancel
Cancels the asynchronous operation

### errback
Fulfills the Deferred instance as an error with the provided error

### isCanceled
Checks whether the deferred has been canceled.

### isFulfilled
Checks whether the deferred has been resolved or rejected.

### isRejected
Checks whether the deferred has been rejected.

### isResolved
Checks whether the deferred has been resolved.

### progress
Send progress events to all listeners

### reject
Fulfills the Deferred instance as an error with the provided error

### resolve
Fulfills the Deferred instance successfully with the provide value

### then
Adds a fulfilledHandler, errorHandler, and progressHandler to be called for
completion of a promise. The fulfilledHandler is called when the promise
is fulfilled. The errorHandler is called when a promise fails. The
progressHandler is called for progress events. All arguments are optional
and non-function values are ignored. The progressHandler is not only an
optional argument, but progress events are purely optional. Promise
providers are not required to ever create progress events.

This function will return a new promise that is fulfilled when the given
fulfilledHandler or errorHandler callback is finished. This allows promise
operations to be chained together. The value returned from the callback
handler is the fulfillment value for the returned promise. If the callback
throws an error, the returned promise will be moved to failed state.


### when
Transparently applies callbacks to values and/or promises.

## Static Properties

### fired


## Static Methods

### addBoth
Add handler as both successful callback and error callback for this deferred instance.

### addCallback
Adds successful callback for this deferred instance.

### addErrback
Adds error callback for this deferred instance.

