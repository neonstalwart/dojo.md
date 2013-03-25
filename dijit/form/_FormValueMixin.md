# Module: dijit/form/_FormValueMixin

*Constructor*

# Constructor

## Summary

Mixin for widgets corresponding to native HTML elements such as `<input>` or `<select>`
that have user changeable values.
## Description

Each _FormValueMixin represents a single input value, and has a (possibly hidden) `<input>` element,
to which it serializes it's input value, so that form submission (either normal submission or via FormBind?)
works as expected.
## Properties

### alt
Corresponds to the native HTML `<input>` element's attribute.

### aria-label


### declaredClass


### disabled
Should this widget respond to user input?
In markup, this is specified as "disabled='disabled'", or just "disabled".

### intermediateChanges
Fires onChange for each value change or only on demand

### name
Name used when submitting form; same as "name" attribute or plain HTML elements

### readOnly
Should this widget respond to user input?
In markup, this is specified as "readOnly".
Similar to disabled except readOnly form values are submitted.

### scrollOnFocus
On focus, should this widget scroll into view?

### tabIndex
Order fields are traversed when user hits the tab key

### type
Corresponds to the native HTML `<input>` element's attribute.

### value
Corresponds to the native HTML `<input>` element's attribute.

## Methods

### compare
Compare 2 values (as returned by get('value') for this widget).

### create


### destroy


### focus
Put focus on this widget

### isFocusable
Tells if this widget is focusable or not.  Used internally by dijit.

### onChange
Callback when this widget's value is changed.

### postCreate


### reset
Reset the widget's value to what it was at initialization time

### undo
Restore the value to the last value passed to onChange

