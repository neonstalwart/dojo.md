# Module: dojo/promise/first

## Summary

Takes multiple promises and returns a new promise that is fulfilled
when the first of these promises is fulfilled.
## Description

Takes multiple promises and returns a new promise that is fulfilled
when the first of these promises is fulfilled. Canceling the returned
promise will *not* cancel any passed promises. The promise will be
fulfilled with the value of the first fulfilled promise.
# Constructor

