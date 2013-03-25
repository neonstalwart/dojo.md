# Module: dijit/_editor/plugins/LinkDialog

*Constructor*

## Properties

### ImgLinkDialog


# Constructor

## Summary

This plugin provides the basis for an 'anchor' (link) dialog and an extension of it
provides the image link dialog.
## Description

The command provided by this plugin is:

- createLink
## Properties

### button
Pointer to `dijit/form/Button` or other widget (ex: `dijit/form/FilteringSelect`)
that is added to the toolbar to control this plugin.
If not specified, will be created on initialization according to `buttonClass`

### buttonClass


### command
String like "insertUnorderedList", "outdent", "justifyCenter", etc. that represents an editor command.
Passed to editor.execCommand() if `useDefaultCommand` is true.

### declaredClass


### disabled
Flag to indicate if this plugin has been disabled and should do nothing
helps control button state, among other things.  Set via the setter api.

### editor
Points to the parent editor

### emailRegExp
Used for validating input as correct email address.  Taken from dojox.validate

### htmlTemplate
String used for templating the HTML to insert at the desired point.

### iconClassPrefix
The CSS class name for the button node is formed from `iconClassPrefix` and `command`

### linkDialogTemplate
Template for contents of TooltipDialog to pick URL

### tag
Tag used for the link type.

### urlRegExp
Used for validating input as correct URL.  While file:// urls are not terribly
useful, they are technically valid.

### useDefaultCommand


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

### setValue
Callback from the dialog when user presses "set" button.

### updateState
Change state of the plugin to respond to events in the editor.

