# Module: dijit/_PaletteMixin

*Constructor*

# Constructor

## Summary

A keyboard accessible palette, for picking a color/emoticon/etc.
## Description

A mixin for a grid showing various entities, so the user can pick a certain entity.
## Properties

### active
True if mouse was pressed while over this widget, and hasn't been released yet

### cellClass
CSS class applied to each cell in the palette

### cssStateNodes
Subclasses may define a cssStateNodes property that lists sub-nodes within the widget that
need CSS classes applied on mouse hover/press and focus.

Each entry in this optional hash is a an attach-point name (like "upArrowButton") mapped to a CSS class name
(like "dijitUpArrowButton"). Example:

    {
    "upArrowButton": "dijitUpArrowButton",
    "downArrowButton": "dijitDownArrowButton"
    }

The above will set the CSS class dijitUpArrowButton to the this.upArrowButton DOMNode when it
is hovered, etc.

### declaredClass


### defaultTimeout
Number of milliseconds before a held key or button becomes typematic

### dyeClass
Constructor for Object created for each cell of the palette.
dyeClass should implement the dijit/_PaletteMixin.__Dye interface.

### hovering
True if cursor is over this widget

### tabIndex
Widget tab index.

### timeoutChangeRate
Fraction of time used to change the typematic timer between events
1.0 means that each typematic event fires at defaultTimeout intervals
Less than 1.0 means that each typematic event fires at an increasing faster rate

### value
Currently selected color/emoticon/etc.

## Methods

### focus
Focus this widget.  Puts focus on the most recently focused cell.

### onChange
Callback when a cell is selected.

### postCreate


