# Module: dijit/Destroyable

*Constructor*

# Constructor

## Summary

Mixin to track handles and release them when instance is destroyed.
## Description

Call this.own(...) on list of handles (returned from dojo/aspect, dojo/on,
dojo/Stateful::watch, or any class (including widgets) with a destroyRecursive() or destroy() method.
Then call destroy() later to destroy this instance and release the resources.
## Properties

### declaredClass


## Methods

### destroy
Destroy this class, releasing any resources registered via own().

### own
Track specified handles and remove/destroy them when this instance is destroyed, unless they were
already removed/destroyed manually.

