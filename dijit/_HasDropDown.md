# Module: dijit/_HasDropDown

*Constructor*

# Constructor

## Summary

Mixin for widgets that need drop down ability.
## Properties

### autoWidth
Set to true to make the drop down at least as wide as this
widget.  Set to false if the drop down should just be its
default width

### declaredClass


### dropDown
The widget to display as a popup.  This widget *must* be
defined before the startup function is called.

### dropDownPosition
This variable controls the position of the drop down.
It's an array of strings with the following values:

- before: places drop down to the left of the target node/widget, or to the right in
the case of RTL scripts like Hebrew and Arabic
- after: places drop down to the right of the target node/widget, or to the left in
the case of RTL scripts like Hebrew and Arabic
- above: drop down goes above target node
- below: drop down goes below target node

The list is positions is tried, in order, until a position is found where the drop down fits
within the viewport.


### forceWidth
Set to true to make the drop down exactly as wide as this
widget.  Overrides autoWidth.

### maxHeight
The max height for our dropdown.
Any dropdown taller than this will have scrollbars.
Set to 0 for no max height, or -1 to limit height to available space in viewport

## Methods

### buildRendering


### closeDropDown
Closes the drop down on this widget

### destroy


### isLoaded
Returns true if the dropdown exists and it's data is loaded.  This can
be overridden in order to force a call to loadDropDown().

### loadAndOpenDropDown
Creates the drop down if it doesn't exist, loads the data
if there's an href and it hasn't been loaded yet, and
then opens the drop down.  This is basically a callback when the
user presses the down arrow button to open the drop down.

### loadDropDown
Creates the drop down if it doesn't exist, loads the data
if there's an href and it hasn't been loaded yet, and then calls
the given callback.

### openDropDown
Opens the dropdown for this widget.   To be called only when this.dropDown
has been created and is ready to display (ie, it's data is loaded).

### postCreate
set up nodes and connect our mouse and keyboard events

### toggleDropDown
Callback when the user presses the down arrow button or presses
the down arrow key to open/close the drop down.
Toggle the drop-down widget; if it is up, close it, if not, open it

