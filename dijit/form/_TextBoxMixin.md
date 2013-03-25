# Module: dijit/form/_TextBoxMixin

*Constructor*

## Methods

### selectInputText
Select text in the input element argument, from start (default 0), to stop (default end).

# Constructor

## Properties

### declaredClass


### displayedValue
For subclasses like ComboBox where the displayed value
(ex: Kentucky) and the serialized value (ex: KY) are different,
this represents the displayed value.

Setting 'displayedValue' through set('displayedValue', ...)
updates 'value', and vice-versa.  Otherwise 'value' is updated
from 'displayedValue' periodically, like onBlur etc.

TODO: move declaration to MappedTextBox?
Problem is that ComboBox references displayedValue,
for benefit of FilteringSelect.

### lowercase
Converts all characters to lowercase if true.  Default is false.

### maxLength
HTML INPUT tag maxLength declaration.

### placeHolder
Defines a hint to help users fill out the input field (as defined in HTML 5).
This should only contain plain text (no html markup).

### propercase
Converts the first character of each word to uppercase if true.

### selectOnClick
If true, all text will be selected when focused with mouse

### trim
Removes leading and trailing whitespace if true.  Default is false.

### uppercase
Converts all characters to uppercase if true.  Default is false.

## Methods

### filter
Auto-corrections (such as trimming) that are applied to textbox
value on blur or form submit.

### format
Replaceable function to convert a value to a properly formatted string.

### onInput
Connect to this function to receive notifications of various user data-input events.
Return false to cancel the event and prevent it from being processed.

### parse
Replaceable function to convert a formatted string to a value

### postCreate


### reset


