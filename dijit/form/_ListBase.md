# Module: dijit/form/_ListBase

*Constructor*

# Constructor

**,*private*

## Summary

Focus-less menu to handle UI events consistently
Abstract methods that must be defined externally:

- onSelect: item is active (mousedown but not yet mouseup, or keyboard arrow selected but no Enter)
- onDeselect:  cancels onSelect
## Properties

### declaredClass


### selected
currently selected node

## Methods

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

