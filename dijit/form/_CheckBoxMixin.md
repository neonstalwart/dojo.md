# Module: dijit/form/_CheckBoxMixin

*Constructor*

# Constructor

## Summary

Mixin to provide widget functionality corresponding to an HTML checkbox

## Description

User interacts with real html inputs.
On onclick (which occurs by mouse click, space-bar, or
using the arrow keys to switch the selected radio button),
we update the state of the checkbox/radio.

## Properties

### declaredClass


### readOnly
Should this widget respond to user input?
In markup, this is specified as "readOnly".
Similar to disabled except readOnly form values are submitted.

### type
type attribute on `<input>` node.
Overrides `dijit/form/Button.type`.  Users should not change this value.

### value
As an initialization parameter, equivalent to value field on normal checkbox
(if checked, the value is passed as the value when form is submitted).

## Methods

### reset


