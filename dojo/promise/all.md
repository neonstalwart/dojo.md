# Module: dojo/promise/all

## Summary

Takes multiple promises and returns a new promise that is fulfilled
when all promises have been fulfilled.
## Description

Takes multiple promises and returns a new promise that is fulfilled
when all promises have been fulfilled. If one of the promises is rejected,
the returned promise is also rejected. Canceling the returned promise will
not* cancel any passed promises.
