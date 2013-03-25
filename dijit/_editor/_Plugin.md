# Module: dijit/_editor/_Plugin

*Constructor*

## Properties

### registry


# Constructor

## Summary

Base class for a "plugin" to the editor, which is usually
a single button on the Toolbar and some associated code
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
If true, this plugin executes by calling Editor.execCommand() with the argument specified in `command`.

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
Change state of the plugin to respond to events in the editor.

