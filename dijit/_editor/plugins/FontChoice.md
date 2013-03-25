# Module: dijit/_editor/plugins/FontChoice

*Constructor*

# Constructor

## Summary

This plugin provides three drop downs for setting style in the editor
(font, font size, and format block), as controlled by command.

## Description

The commands provided by this plugin are:

- fontName: Provides a drop down to select from a list of font names
- fontSize: Provides a drop down to select from a list of font sizes
- formatBlock: Provides a drop down to select from a list of block styles
which can easily be added to an editor by including one or more of the above commands
in the `plugins` attribute as follows:


    plugins="['fontName','fontSize',...]"


It is possible to override the default dropdown list by providing an Array for the `custom` property when
instantiating this plugin, e.g.


    plugins="[{name:'dijit._editor.plugins.FontChoice', command:'fontName', values:['Verdana','Myriad','Garamond']},...]"


Alternatively, for `fontName` only, `generic:true` may be specified to provide a dropdown with
[CSS generic font families](http://www.w3.org/TR/REC-CSS2/fonts.html#generic-font-families).

Note that the editor is often unable to properly handle font styling information defined outside
the context of the current editor instance, such as pre-populated HTML.
## Properties

### button
Pointer to `dijit/form/Button` or other widget (ex: `dijit/form/FilteringSelect`)
that is added to the toolbar to control this plugin.
If not specified, will be created on initialization according to `buttonClass`

### buttonClass
Class of widget (ex: dijit.form.Button or dijit/form/FilteringSelect)
that is added to the toolbar to control this plugin.
This is used to instantiate the button, unless `button` itself is specified directly.

### command
String like "insertUnorderedList", "outdent", "justifyCenter", etc. that represents an editor command.
Passed to editor.execCommand() if `useDefaultCommand` is true.

### declaredClass


### disabled
Flag to indicate if this plugin has been disabled and should do nothing
helps control button state, among other things.  Set via the setter api.

### editor
Points to the parent editor

### iconClassPrefix
The CSS class name for the button node is formed from `iconClassPrefix` and `command`

### useDefaultCommand
Override _Plugin.useDefaultCommand...
processing is handled by this plugin, not by dijit/Editor.

## Methods

### connect
Deprecated.  Use this.own() with dojo/on or dojo/aspect.instead.

Make a connect.connect() that is automatically disconnected when this plugin is destroyed.
Similar to `dijit/_Widget.connect()`.

### destroy


### get
Get a property from a plugin.

### getLabel
Returns the label to use for the button

### own
Track specified handles and remove/destroy them when this instance is destroyed, unless they were
already removed/destroyed manually.

### set
Set a property on a plugin

### setEditor
Tell the plugin which Editor it is associated with.

### setToolbar
Tell the plugin to add it's controller widget (often a button)
to the toolbar.  Does nothing if there is no controller widget.

### updateState
Overrides _Plugin.updateState().  This controls updating the menu
options to the right values on state changes in the document (that trigger a
test of the actions.)
It set value of drop down in toolbar to reflect font/font size/format block
of text at current caret position.

