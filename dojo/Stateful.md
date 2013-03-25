# dojo/Stateful

*Constructor*

## Summary

Base class for objects that provide named properties with optional getter/setter
control and the ability to watch for property changes

The class also provides the functionality to auto-magically manage getters
and setters for object attributes/properties.

Getters and Setters should follow the format of _xxxGetter or _xxxSetter where
the xxx is a name of the attribute to handle.  So an attribute of "foo"
would have a custom getter of _fooGetter and a custom setter of _fooSetter.

## Static Properties

### _attrPairNames
Used across all instances a hash to cache attribute names and their getter 
and setter names.

### declaredClass


## Static Methods

### _changeAttrValue
Internal helper for directly changing an attribute value.


### _get
Private function that does a get based off a hash of names

### _getAttrNames
Helper function for get() and set().
Caches attribute name values so we don't do the string ops every time.

### get
Get a property on a Stateful instance.

### postscript


### set
Set a property on a Stateful instance

### watch
Watches a property for changes

