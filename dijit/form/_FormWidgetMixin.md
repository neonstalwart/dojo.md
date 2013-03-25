# Module: dijit/form/_FormWidgetMixin

*Constructor*

# Constructor

## Summary

Mixin for widgets corresponding to native HTML elements such as `<checkbox>` or `<button>`,
which can be children of a `<form>` node or a `dijit/form/Form` widget.

## Description

Represents a single HTML element.
All these widgets should have these attributes just like native HTML input elements.
You can set them during widget construction or afterwards, via `dijit/_WidgetBase.set()`.

They also share some common methods.
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

