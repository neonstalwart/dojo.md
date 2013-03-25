# Module: dijit/form/_FormMixin

*Constructor*

# Constructor

## Summary

Mixin for containers of form widgets (i.e. widgets that represent a single value
and can be children of a `<form>` node or `dijit/form/Form` widget)
## Description

Can extract all the form widgets
values and combine them into a single javascript object, or alternately
take such an object and set the values for all the contained
form widgets
## Properties

### declaredClass


### state
Will be "Error" if one or more of the child widgets has an invalid value,
"Incomplete" if not all of the required child widgets are filled in.  Otherwise, "",
which indicates that the form is ready to be submitted.

## Methods

### connectChildren
You can call this function directly, ex. in the event that you
programmatically add a widget to the form *after* the form has been
initialized.

### destroy


### disconnectChildren
Deprecated method.   Applications no longer need to call this.   Remove for 2.0.

### getValues


### isValid
Returns true if all of the widgets are valid.
Deprecated, will be removed in 2.0.  Use get("state") instead.

### onValidStateChange
Stub function to connect to if you want to do something
(like disable/enable a submit button) when the valid
state changes on the form as a whole.

Deprecated.  Will be removed in 2.0.  Use watch("state", ...) instead.

### reset


### setValues


### startup


### validate
returns if the form is valid - same as isValid - but
provides a few additional (ui-specific) features:

1. it will highlight any sub-widgets that are not valid
2. it will call focus() on the first invalid sub-widget

