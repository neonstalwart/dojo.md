# dojo/DeferredList

## Summary

Deprecated, use dojo/promise/all instead.
Provides event handling for a group of Deferred objects.
## Description

DeferredList takes an array of existing deferreds and returns a new deferred of its own
this new deferred will typically have its callback fired when all of the deferreds in
the given list have fired their own deferreds.  The parameters `fireOnOneCallback` and
fireOnOneErrback, will fire before all the deferreds as appropriate
## Static Methods

### gatherResults
Gathers the results of the deferreds for packaging
as the parameters to the Deferred Lists' callback

