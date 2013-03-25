# Module: dojo/touch

## Summary

This module provides unified touch event handlers by exporting
press, move, release and cancel which can also run well on desktop.
Based on http://dvcs.w3.org/hg/webevents/raw-file/tip/touchevents.html
Also, if the dojoClick property is set to true on a DOM node, dojo/touch generates
click events immediately for this node and its descendants, to avoid the
delay before native browser click events, and regardless of whether evt.preventDefault()
was called in a touch.press event listener.

## Methods

### cancel
Register a listener to 'touchcancel'|'mouseleave' for the given node

### enter
Register a listener to mouse.enter or touch equivalent for the given node

### leave
Register a listener to mouse.leave or touch equivalent for the given node

### move
Register a listener that fires when the mouse cursor or a finger is dragged over the given node.

### out
Register a listener to 'mouseout' or touch equivalent for the given node

### over
Register a listener to 'mouseover' or touch equivalent for the given node

### press
Register a listener to 'touchstart'|'mousedown' for the given node

### release
Register a listener to releasing the mouse button while the cursor is over the given node
(i.e. "mouseup") or for removing the finger from the screen while touching the given node.

