# Module: dojo/_base/event

## Summary

This module defines dojo DOM event API.   Usually you should use dojo/on, and evt.stopPropagation() +
evt.preventDefault(), rather than this module.
## Methods

### fix
normalizes properties on the event object including event
bubbling methods, keystroke normalization, and x/y positions

### stop
prevents propagation and clobbers the default action of the
passed event

