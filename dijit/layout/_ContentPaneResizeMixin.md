# Module: dijit/layout/_ContentPaneResizeMixin

*Constructor*

# Constructor

## Summary

Resize() functionality of ContentPane.   If there's a single layout widget
child then it will call resize() with the same dimensions as the ContentPane.
Otherwise just calls resize on each child.

Also implements basic startup() functionality, where starting the parent
will start the children
## Properties

### declaredClass


### doLayout
- false - don't adjust size of children
- true - if there is a single visible child widget, set it's size to however big the ContentPane is

### isLayoutContainer
Indicates that this widget will call resize() on it's child widgets
when they become visible.

## Methods

### resize
See `dijit/layout/_LayoutWidget.resize()` for description.
Although ContentPane doesn't extend _LayoutWidget, it does implement
the same API.

### startup
See `dijit/layout/_LayoutWidget.startup()` for description.
Although ContentPane doesn't extend _LayoutWidget, it does implement
the same API.

