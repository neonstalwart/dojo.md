# Module: dijit/main

## Summary

The dijit package main module.
Deprecated.   Users should access individual modules (ex: dijit/registry) directly.
## Properties

### defaultDuration
The default fx.animation speed (in ms) to use for all Dijit
transitional fx.animations, unless otherwise specified
on a per-instance basis. Defaults to 200, overrided by
`djConfig.defaultDuration`

### place
Code to place a DOMNode relative to another DOMNode.
Load using require(["dijit/place"], function(place){ ... }).

### popup


### registry
Registry of existing widget on page, plus some utility methods.

### typematic
These functions are used to repetitively call a user specified callback
method when a specific key or mouse click over a specific DOM node is
held down for a specific amount of time.
Only 1 such event is allowed to occur on the browser page at 1 time.

## Methods

### BackgroundIframe
For IE/FF z-index schenanigans. id attribute is required.


### focus


### getBookmark
Retrieves a bookmark that can be used with moveToBookmark to return to the same range

### getDocumentWindow


### getFirstInTabbingOrder
Finds the descendant of the specified root node
that is first in the tabbing order

### getFocus
Called as getFocus(), this returns an Object showing the current focus
and selected text.

Called as getFocus(widget), where widget is a (widget representing) a button
that was just pressed, it returns where focus was before that button
was pressed.   (Pressing the button may have either shifted focus to the button,
or removed focus altogether.)   In this case the selected text is not returned,
since it can't be accurately determined.


### getLastInTabbingOrder
Finds the descendant of the specified root node
that is last in the tabbing order

### getPopupAroundAlignment
Deprecated method, unneeded when using dijit/place directly.
Transforms the passed array of preferred positions into a format suitable for
passing as the aroundCorners argument to dijit/place.placeOnScreenAroundElement.

### getViewport
Deprecated method to return the dimensions and scroll position of the viewable area of a browser window.
New code should use windowUtils.getBox()

### getWaiRole
Gets the role for an element (which should be a wai role).

### getWaiState
Gets the value of a state on an element.

### hasDefaultTabStop
Tests if element is tab-navigable even without an explicit tabIndex setting

### hasWaiRole
Determines if an element has a particular role.

### hasWaiState
Determines if an element has a given state.

### hideTooltip
Static method to hide the tooltip displayed via showTooltip()

### isCollapsed
Returns true if there is no text selected

### isTabNavigable
Tests if an element is tab-navigable

### moveToBookmark
Moves current selection to a bookmark

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

### registerIframe
Registers listeners on the specified iframe so that any click
or focus event on that iframe (or anything in it) is reported
as a focus/click event on the `<iframe>` itself.

### registerWin
Registers listeners on the specified window (either the main
window or an iframe's window) to detect when the user has clicked somewhere
or focused somewhere.

### removeWaiRole
Removes the specified role from an element.
Removes role attribute if no specific role provided (for backwards compat.)

### removeWaiState
Removes a state from an element.

### scrollIntoView
Scroll the passed node into view, if it is not already.
Deprecated, use `windowUtils.scrollIntoView` instead.

### selectInputText
Select text in the input element argument, from start (default 0), to stop (default end).

### setWaiRole
Sets the role on an element.

### setWaiState
Sets a state on an element.

### showTooltip
Static method to display tooltip w/specified contents in specified position.
See description of dijit/Tooltip.defaultPosition for details on position parameter.
If position is not specified then dijit/Tooltip.defaultPosition is used.

### unregisterIframe
Unregisters listeners on the specified iframe created by registerIframe.
After calling be sure to delete or null out the handle itself.

### unregisterWin
Unregisters listeners on the specified window (either the main
window or an iframe's window) according to handle returned from registerWin().
After calling be sure to delete or null out the handle itself.

