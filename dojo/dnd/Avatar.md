# dojo/dnd/Avatar

*Constructor*

## Summary

Object that represents transferred DnD items visually
## Static Properties

### declaredClass


### manager
a DnD manager object

## Static Methods

### _generateText
generates a proper text to reflect copying or moving of items

### construct
constructor function;
it is separate so it can be (dynamically) overwritten in case of need

### destroy
destructor for the avatar; called to remove all references so it can be garbage-collected

### update
updates the avatar to reflect the current DnD state
