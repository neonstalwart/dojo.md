# Module: dijit/_BidiMixin

## Summary

When has("dojo-bidi") is true, _WidgetBase will mixin this class.   It enables support for the textdir
property to control text direction independently from the GUI direction.
## Description

There's a special need for displaying BIDI text in rtl direction
in ltr GUI, sometimes needed auto support.
In creation of widget, if it's want to activate this class,
the widget should define the "textDir".
## Properties

### textDir
Bi-directional support,  the main variable which is responsible for the direction of the text.
The text direction can be different than the GUI direction by using this parameter in creation
of a widget.

Allowed values:

1. "ltr"
2. "rtl"
3. "auto" - contextual the direction of a text defined by first strong letter.

By default is as the page direction.

## Methods

### applyTextDir
Set element.dir according to this.textDir, assuming this.textDir has a value.

### enforceTextDirWithUcc
Wraps by UCC (Unicode control characters) option's text according to this.textDir

### getTextDir
Gets the right direction of text.

### restoreOriginalText
Restores the text of origObj, if needed, after enforceTextDirWithUcc, e.g. set("textDir", textDir).

