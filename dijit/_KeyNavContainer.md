# Module: dijit/_KeyNavContainer

*Constructor*

# Constructor

## Summary

A _Container with keyboard navigation of its children.
## Description

Provides normalized keyboard and focusing code for Container widgets.
To use this mixin, call connectKeyNavHandlers() in postCreate().
Also, child widgets must implement a focus() method.
## Properties

### declaredClass


### focusedChild
The currently focused child widget, or null if there isn't one

### multiCharSearchDuration
If multiple characters are typed where each keystroke happens within
multiCharSearchDuration of the previous keystroke,
search for nodes matching all the keystrokes.

For example, typing "ab" will search for entries starting with
"ab" unless the delay between "a" and "b" is greater than multiCharSearchDuration.

### tabIndex
Tab index of the container; same as HTML tabIndex attribute.
Note then when user tabs into the container, focus is immediately
moved to the first item in the container.

## Methods

### addChild


### buildRendering


### childSelector


### connectKeyNavHandlers
Call in postCreate() to attach the keyboard handlers to the container.

### focus
Default focus() implementation: focus the first child.

### focusChild
Focus specified child widget.

### focusFirstChild
Focus the first focusable child in the container.

### focusLastChild
Focus the last focusable child in the container.

### focusNext
Focus the next widget

### focusPrev
Focus the last focusable node in the previous widget
(ex: go to the ComboButton icon section rather than button section)

### getIndexOfChild
Gets the index of the child in this container or -1 if not found

### hasChildren
Returns true if widget has child widgets, i.e. if this.containerNode contains widgets.

### onKeyboardSearch
When a key is pressed that matches a child item,
this method is called so that a widget can take appropriate action is necessary.

### postCreate


### removeChild
Removes the passed widget instance from this widget but does
not destroy it.  You can also pass in an integer indicating
the index within the container to remove (ie, removeChild(5) removes the sixth widget).

### startup


### startupKeyNavChildren


