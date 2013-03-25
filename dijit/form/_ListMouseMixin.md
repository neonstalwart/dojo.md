# Module: dijit/form/_ListMouseMixin

*Constructor*

# Constructor

**,*private*

## Summary

A mixin to handle mouse or touch events for a focus-less menu
Abstract methods that must be defined externally:

- onClick: item was chosen (mousedown somewhere on the menu and mouseup somewhere on the menu)
## Properties

### declaredClass


### selected
currently selected node

## Methods

### postCreate


### selectFirstNode
Select the first displayed item in the list.

### selectLastNode
Select the last displayed item in the list

### selectNextNode
Select the item just below the current selection.
If nothing selected, select first node.

### selectPreviousNode
Select the item just above the current selection.
If nothing selected, select last node (if
you select Previous and try to keep scrolling up the list).

