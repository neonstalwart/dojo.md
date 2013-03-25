# Module: dojo/touch

## Summary

This module provides unified touch event handlers by exporting
press, move, release and cancel which can also run well on desktop.
Based on http://dvcs.w3.org/hg/webevents/raw-file/tip/touchevents.html
Also, if the dojoClick property is set to true on a DOM node, dojo/touch generates
click events immediately for this node and its descendants, to avoid the
delay before native browser click events, and regardless of whether evt.preventDefault()
was called in a touch.press event listener.

## Examples

Used with dojo.on

      define(["dojo/on", "dojo/touch"], function(on, touch){
        on(node, touch.press, function(e){});
        on(node, touch.move, function(e){});
        on(node, touch.release, function(e){});
        on(node, touch.cancel, function(e){});

---

Used with touch.* directly

      touch.press(node, function(e){});
      touch.move(node, function(e){});
      touch.release(node, function(e){});
      touch.cancel(node, function(e){});

---

Have dojo/touch generate clicks without delay, with a default move threshold of 4 pixels

      node.dojoClick = true;

---

Have dojo/touch generate clicks without delay, with a move threshold of 10 pixels horizontally and vertically

      node.dojoClick = 10;

---

Have dojo/touch generate clicks without delay, with a move threshold of 50 pixels horizontally and 10 pixels vertically

      node.dojoClick = {x:50, y:5};
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

