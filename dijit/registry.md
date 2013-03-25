# Module: dijit/registry

## Summary

Registry of existing widget on page, plus some utility methods.
## Properties

### length
Number of registered widgets

## Methods

### add
Add a widget to the registry. If a duplicate ID is detected, a error is thrown.

### byId
Find a widget by it's id.
If passed a widget then just returns the widget.

### byNode
Returns the widget corresponding to the given DOMNode

### findWidgets
Search subtree under root returning widgets found.
Doesn't search for nested widgets (ie, widgets inside other widgets).

### getEnclosingWidget
Returns the widget whose DOM tree contains the specified DOMNode, or null if
the node is not contained within the DOM tree of any widget

### getUniqueId
Generates a unique id for a given widgetType

### remove
Remove a widget from the registry. Does not destroy the widget; simply
removes the reference.

### toArray
Convert registry into a true Array


