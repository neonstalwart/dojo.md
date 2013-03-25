# Module: dojo/request/watch

## Summary

Watches the io request represented by dfd to see if it completes.
## Methods

### cancelAll
Cancels all pending IO requests, regardless of IO type

# Constructor

## Properties

### ioCheck
Function used to check if basic IO call worked. Gets the dfd
object as its only argument.

### resHandle
Function used to process response. Gets the dfd
object as its only argument.

### validCheck
Function used to check if the IO request is still valid. Gets the dfd
object as its only argument.

