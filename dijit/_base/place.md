# Module: dijit/_base/place

## Summary

Deprecated back compatibility module, new code should use dijit/place directly instead of using this module.
## Methods

### getPopupAroundAlignment
Deprecated method, unneeded when using dijit/place directly.
Transforms the passed array of preferred positions into a format suitable for
passing as the aroundCorners argument to dijit/place.placeOnScreenAroundElement.

### getViewport
Deprecated method to return the dimensions and scroll position of the viewable area of a browser window.
New code should use windowUtils.getBox()

### placeOnScreen
Positions node kitty-corner to the rectangle centered at (pos.x, pos.y) with width and height of
padding.x * 2 and padding.y * 2, or zero if padding not specified.  Picks first corner in corners[]
where node is fully visible, or the corner where it's most visible.

Node is assumed to be absolutely or relatively positioned.

### placeOnScreenAroundElement
Like dijit.placeOnScreenAroundNode(), except it accepts an arbitrary object
for the "around" argument and finds a proper processor to place a node.
Deprecated, new code should use dijit/place.around() instead.

### placeOnScreenAroundNode
Position node adjacent or kitty-corner to aroundNode
such that it's fully visible in viewport.
Deprecated, new code should use dijit/place.around() instead.

### placeOnScreenAroundRectangle
Like dijit.placeOnScreenAroundNode(), except that the "around"
parameter is an arbitrary rectangle on the screen (x, y, width, height)
instead of a dom node.
Deprecated, new code should use dijit/place.around() instead.

