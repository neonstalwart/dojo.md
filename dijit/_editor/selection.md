# Module: dijit/_editor/selection

## Summary

Deprecated text selection API.  Will be removed in 2.0.  New code should use dijit/selection.
## Methods

### collapse
Function to collapse (clear), the current selection

### getAncestorElement
Return the parent element of the current selection which is of
type tagName (or one of the other specified tagName)

### getParentElement
Get the parent element of the current selection

### getParentOfType
Function to locate a parent node that matches one of a set of tags

### getSelectedElement
Retrieves the selected element (if any), just in the case that
a single element (object like and image or a table) is
selected.

### getSelectedHtml
Return the html text of the current selection or null if unavailable

### getSelectedText
Return the text (no html tags) included in the current selection or null if no text is selected

### getType
Get the selection type (like win.doc.select.type in IE).

### hasAncestorElement
Check whether current selection has a  parent element which is
of type tagName (or one of the other specified tagName)

### inSelection
This function determines if 'node' is
in the current selection.

### isTag
Function to determine if a node is one of an array of tags.

### remove
Function to delete the currently selected content from the document.

### selectElement
clear previous selection and select element (including all its children)

### selectElementChildren
clear previous selection and select the content of the node
(excluding the node itself)

