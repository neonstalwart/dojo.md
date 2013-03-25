# Module: dojo/mouse

## Summary

This module provide mouse event handling utility functions and exports
mouseenter and mouseleave event emulation.
## Examples

* To use these events, you register a mouseenter like this:

      define(["dojo/on", dojo/mouse"], function(on, mouse){
        on(targetNode, mouse.enter, function(event){
          dojo.addClass(targetNode, "highlighted");
        });
        on(targetNode, mouse.leave, function(event){
          dojo.removeClass(targetNode, "highlighted");
        });


## Properties

### enter
This is an extension event for the mouseenter that IE provides, emulating the
behavior on other browsers.

### leave
This is an extension event for the mouseleave that IE provides, emulating the
behavior on other browsers.

## Methods

### isLeft
Test an event object (from a mousedown event) to see if the left button was pressed.

### isMiddle
Test an event object (from a mousedown event) to see if the middle button was pressed.

### isRight
Test an event object (from a mousedown event) to see if the right button was pressed.

### wheel
This is an extension event for the mousewheel that non-Mozilla browsers provide,
emulating the behavior on Mozilla based browsers.

