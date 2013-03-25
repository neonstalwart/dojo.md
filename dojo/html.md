# dojo/html

## Summary

TODOC
## Static Properties

### _ContentSetter


## Static Methods

### _emptyNode
Removes all child nodes from the given node.   Deprecated, should use dojo/dom-constuct.empty() directly
instead.

### _secureForInnerHtml
removes !DOCTYPE and title elements from the html string.

khtml is picky about dom faults, you can't attach a style or `<title>` node as child of body
must go into head, so we need to cut out those tags

### _setNodeContent
inserts the given content into the given node

### set
inserts (replaces) the given content into the given node. dojo.place(cont, node, "only")
may be a better choice for simple HTML insertion.

## Static Methods

### hasOwnProperty


### toString


