# dojo/_base/lang

## Summary

This module defines Javascript language extensions.
## Static Properties

### _extraNames
Lists property names that must be explicitly processed during for-in iteration
in environments that have has("bug-for-in-skips-shadowed") true.

## Static Methods

### _hitchArgs


### _mixin
Copies/adds all properties of source to dest; returns dest.

### _toArray
Converts an array-like object (i.e. arguments, DOMCollection) to an
array. Returns a new Array with the elements of obj.

### clone
Clones objects (including DOM nodes) and all children.
Warning: do not clone cyclic structures.

### delegate
Returns a new object which "looks" to obj for properties which it
does not have a value for. Optionally takes a bag of properties to
seed the returned object with initially.

### exists
determine if an object supports a given method

### extend
Adds all properties and methods of props to constructor's
prototype, making them available to all instances created with
constructor.

### getObject
Get a property from a dot-separated string, such as "A.B.C"

### hitch
Returns a function that will only ever execute in the a given scope.
This allows for easy use of object member functions
in callbacks and other places in which the "this" keyword may
otherwise not reference the expected scope.
Any number of default positional arguments may be passed as parameters
beyond "method".
Each of these values will be used to "placehold" (similar to curry)
for the hitched function.

### isAlien
Returns true if it is a built-in function or some other kind of
oddball that *should* report as a function but doesn't

### isArray
Return true if it is an Array.
Does not work on Arrays created in other windows.

### isArrayLike
similar to isArray() but more permissive

### isFunction
Return true if it is a Function

### isObject
Returns true if it is a JavaScript object (or an Array, a Function
or null)

### isString
Return true if it is a String

### mixin
Copies/adds all properties of one or more sources to dest; returns dest.

### partial
similar to hitch() except that the scope object is left to be
whatever the execution context eventually becomes.

### replace
Performs parameterized substitutions on a string. Throws an
exception if any parameter is unmatched.

### setObject
Set a property from a dot-separated string, such as "A.B.C"

### trim
Trims whitespace from both sides of the string

## Static Methods

### hasOwnProperty


### toString


