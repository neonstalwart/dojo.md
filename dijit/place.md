# Module: dijit/place

## Summary

Code to place a DOMNode relative to another DOMNode.
Load using require(["dijit/place"], function(place){ ... }).
## Methods

### around
Position node adjacent or kitty-corner to anchor
such that it's fully visible in viewport.

### at
Positions node kitty-corner to the rectangle centered at (pos.x, pos.y) with width and height of
padding.x * 2 and padding.y * 2, or zero if padding not specified.  Picks first corner in corners[]
where node is fully visible, or the corner where it's most visible.

Node is assumed to be absolutely or relatively positioned.

