# Module: dojo/Stateful

*Constructor*

# Constructor

## Summary

Base class for objects that provide named properties with optional getter/setter
control and the ability to watch for property changes

The class also provides the functionality to auto-magically manage getters
and setters for object attributes/properties.

Getters and Setters should follow the format of _xxxGetter or _xxxSetter where
the xxx is a name of the attribute to handle.  So an attribute of "foo"
would have a custom getter of _fooGetter and a custom setter of _fooSetter.

## Properties

### declaredClass


## Methods

### get
Get a property on a Stateful instance.

### postscript


### set
Set a property on a Stateful instance

### watch
Watches a property for changes

