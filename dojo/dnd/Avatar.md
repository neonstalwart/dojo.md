# Module: dojo/dnd/Avatar

*Constructor*

# Constructor

## Summary

Object that represents transferred DnD items visually
## Properties

### declaredClass


### manager
a DnD manager object

## Methods

### construct
constructor function;
it is separate so it can be (dynamically) overwritten in case of need

### destroy
destructor for the avatar; called to remove all references so it can be garbage-collected

### update
updates the avatar to reflect the current DnD state

