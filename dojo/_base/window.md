# dojo/_base/window

## Summary

API to save/set/restore the global/document scope.
## Static Properties

### doc
Alias for the current document. 'doc' can be modified
for temporary context shifting. See also withDoc().

### global
Alias for the current window. 'global' can be modified
for temporary context shifting. See also withGlobal().

## Static Methods

### body
Return the body element of the specified document or of dojo/_base/window::doc.

### setContext
changes the behavior of many core Dojo functions that deal with
namespace and DOM lookup, changing them to work in a new global
context (e.g., an iframe). The varibles dojo.global and dojo.doc
are modified as a result of calling this function and the result of
`dojo.body()` likewise differs.

### withDoc
Invoke callback with documentObject as dojo/_base/window::doc.

### withGlobal
Invoke callback with globalObject as dojo.global and
globalObject.document as dojo.doc.

## Static Methods

### hasOwnProperty


### toString


