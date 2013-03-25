# Module: dijit/_KeyNavMixin

*Constructor*

# Constructor

## Summary

A mixin to allow arrow key and letter key navigation of child or descendant widgets.
It can be used by dijit/_Container based widgets with a flat list of children,
or more complex widgets like dijit/Tree.

To use this mixin, the subclass must:

- Implement  _getNext(), _getFirst(), _getLast(), _onLeftArrow(), _onRightArrow()
_onDownArrow(), _onUpArrow() methods to handle home/end/left/right/up/down keystrokes.
Next and previous in this context refer to a linear ordering of the descendants used
by letter key search.
- Set all descendants' initial tabIndex to "-1"; both initial descendants and any
descendants added later, by for example addChild()
- Define childSelector to a function or string that identifies focusable descendant widgets

Also, child widgets must implement a focus() method.
## Properties

### childSelector
Selector (passed to on.selector()) used to identify what to treat as a child widget.   Used to monitor
focus events and set this.focusedChild.   Must be set by implementing class.   If this is a string
(ex: "> *") then the implementing class must require dojo/query.

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

### focus
Default focus() implementation: focus the first child.

### focusChild
Focus specified child widget.

### focusFirstChild
Focus the first focusable child in the container.

### focusLastChild
Focus the last focusable child in the container.

### onKeyboardSearch
When a key is pressed that matches a child item,
this method is called so that a widget can take appropriate action is necessary.

### postCreate


