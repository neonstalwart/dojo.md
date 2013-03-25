# Module: dojo/dom-geometry

## Summary

This module defines the core dojo DOM geometry API.
## Properties

### boxModel


## Methods

### docScroll
Returns an object with {node, x, y} with corresponding offsets.

### fixIeBiDiScrollLeft
In RTL direction, scrollLeft should be a negative value, but IE
returns a positive one. All codes using documentElement.scrollLeft
must call this function to fix this error, otherwise the position
will offset to right when there is a horizontal scrollbar.

### getBorderExtents
returns an object with properties useful for noting the border
dimensions.

### getContentBox
Returns an object that encodes the width, height, left and top
positions of the node's content box, irrespective of the
current box model.

### getIeDocumentElementOffset
returns the offset in x and y from the document body to the
visual edge of the page for IE

### getMarginBox
returns an object that encodes the width, height, left and top
positions of the node's margin box.

### getMarginExtents
returns object with properties useful for box fitting with
regards to box margins (i.e., the outer-box).

- l/t = marginLeft, marginTop, respectively
- w = total width, margin inclusive
- h = total height, margin inclusive

The w/h are used for calculating boxes.
Normally application code will not need to invoke this
directly, and will use the ...box... functions instead.

### getMarginSize
returns an object that encodes the width and height of
the node's margin box

### getPadBorderExtents
Returns object with properties useful for box fitting with
regards to padding.

### getPadExtents
Returns object with special values specifically useful for node
fitting.

### isBodyLtr
Returns true if the current language is left-to-right, and false otherwise.

### normalizeEvent
Normalizes the geometry of a DOM event, normalizing the pageX, pageY,
offsetX, offsetY, layerX, and layerX properties

### position
Gets the position and size of the passed element relative to
the viewport (if includeScroll==false), or relative to the
document root (if includeScroll==true).


### setContentSize
Sets the size of the node's contents, irrespective of margins,
padding, or borders.

### setMarginBox
sets the size of the node's margin box and placement
(left/top), irrespective of box model. Think of it as a
passthrough to setBox that handles box-model vagaries for
you.

# Constructor

## Methods

### hasOwnProperty


