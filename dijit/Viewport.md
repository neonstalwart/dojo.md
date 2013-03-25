# Module: dijit/Viewport

## Summary

Utility singleton to watch for viewport resizes, avoiding duplicate notifications
which can lead to infinite loops.
## Description

Usage: Viewport.on("resize", myCallback).

myCallback() is called without arguments in case it's _WidgetBase.resize(),
which would interpret the argument as the size to make the widget.
