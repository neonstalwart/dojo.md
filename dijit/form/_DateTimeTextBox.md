# Module: dijit/form/_DateTimeTextBox

*Constructor*

# Constructor

## Summary

Base class for validating, serializable, range-bound date or time text box.
## Properties

### active
True if mouse was pressed while over this widget, and hasn't been released yet

### alt
Corresponds to the native HTML `<input>` element's attribute.

### aria-label


### attachScope
Object to which attach points and events will be scoped.  Defaults
to 'this'.

### attributeMap
Deprecated.  Instead of attributeMap, widget should have a _setXXXAttr attribute
for each XXX attribute to be mapped to the DOM.

attributeMap sets up a "binding" between attributes (aka properties)
of the widget and the widget's DOM.
Changes to widget attributes listed in attributeMap will be
reflected into the DOM.

For example, calling set('title', 'hello')
on a TitlePane will automatically cause the TitlePane's DOM to update
with the new title.

attributeMap is a hash where the key is an attribute of the widget,
and the value reflects a binding to a:

- DOM node attribute

    focus: {node: "focusNode", type: "attribute"}

Maps this.focus to this.focusNode.focus

- DOM node innerHTML

    title: { node: "titleNode", type: "innerHTML" }

Maps this.title to this.titleNode.innerHTML

- DOM node innerText

    title: { node: "titleNode", type: "innerText" }

Maps this.title to this.titleNode.innerText

- DOM node CSS class

    myClass: { node: "domNode", type: "class" }

Maps this.myClass to this.domNode.className

If the value is an array, then each element in the array matches one of the
formats of the above list.

There are also some shorthands for backwards compatibility:

- string --> { node: string, type: "attribute" }, for example:


    "focusNode" ---> { node: "focusNode", type: "attribute" }


- "" --> { node: "domNode", type: "attribute" }

### autoWidth


### baseClass


### class


### constraints
Despite the name, this parameter specifies both constraints on the input
(including starting/ending dates/times allowed) as well as
formatting options like whether the date is displayed in long (ex: December 25, 2005)
or short (ex: 12/25/2005) format.  See `dijit/form/_DateTimeTextBox.__Constraints` for details.

### containerNode
Designates where children of the source DOM node will be placed.
"Children" in this case refers to both DOM nodes and widgets.
For example, for myWidget:


    <div data-dojo-type=myWidget>
    <b> here's a plain DOM node
    <span data-dojo-type=subWidget>and a widget</span>
    <i> and another plain DOM node </i>
    </div>


containerNode would point to:


    <b> here's a plain DOM node
    <span data-dojo-type=subWidget>and a widget</span>
    <i> and another plain DOM node </i>


In templated widgets, "containerNode" is set via a
data-dojo-attach-point assignment.

containerNode must be defined for any widget that accepts innerHTML
(like ContentPane or BorderContainer or even Button), and conversely
is null for widgets that don't, like TextBox.

### cssStateNodes


### datePackage
JavaScript namespace to find calendar routines.   If unspecified, uses Gregorian calendar routines
at dojo/date and dojo/date/locale.

### declaredClass


### dir
Bi-directional support, as defined by the [HTML DIR](http://www.w3.org/TR/html401/struct/dirlang.html#adef-dir)
attribute. Either left-to-right "ltr" or right-to-left "rtl".  If undefined, widgets renders in page's
default direction.

### disabled
Should this widget respond to user input?
In markup, this is specified as "disabled='disabled'", or just "disabled".

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

### domNode
This is our visible representation of the widget! Other DOM
Nodes may by assigned to other properties, usually through the
template system's data-dojo-attach-point syntax, but the domNode
property is the canonical "top level" node in widget UI.

### dropDown
The widget to display as a popup.  This widget *must* be
defined before the startup function is called.

### dropDownDefaultValue
The default value to focus in the popupClass widget when the textbox value is empty.

### dropDownPosition
This variable controls the position of the drop down.
It's an array of strings with the following values:

- before: places drop down to the left of the target node/widget, or to the right in
the case of RTL scripts like Hebrew and Arabic
- after: places drop down to the right of the target node/widget, or to the left in
the case of RTL scripts like Hebrew and Arabic
- above: drop down goes above target node
- below: drop down goes below target node

The list is positions is tried, in order, until a position is found where the drop down fits
within the viewport.


### focused
This widget or a widget it contains has focus, or is "active" because
it was recently clicked.

### forceWidth
Set to true to make the drop down exactly as wide as this
widget.  Overrides autoWidth.

### hasDownArrow
Set this textbox to display a down arrow button, to open the drop down list.

### hovering
True if cursor is over this widget

### id
A unique, opaque ID string that can be assigned by users or by the
system. If the developer passes an ID which is known not to be
unique, the specified ID is ignored and the system-generated ID is
used instead.

### intermediateChanges
Fires onChange for each value change or only on demand

### invalidMessage
The message to display if value is invalid.
The translated string value is read from the message file by default.
Set to "" to use the promptMessage instead.

### lang
Rarely used.  Overrides the default Dojo locale used to render this widget,
as defined by the [HTML LANG](http://www.w3.org/TR/html401/struct/dirlang.html#adef-lang) attribute.
Value must be among the list of locales specified during by the Dojo bootstrap,
formatted according to [RFC 3066](http://www.ietf.org/rfc/rfc3066.txt) (like en-us).

### lowercase
Converts all characters to lowercase if true.  Default is false.

### maxHeight
The max height for our dropdown.
Any dropdown taller than this will have scrollbars.
Set to 0 for no max height, or -1 to limit height to available space in viewport

### maxLength
HTML INPUT tag maxLength declaration.

### message
Currently error/prompt message.
When using the default tooltip implementation, this will only be
displayed when the field is focused.

### missingMessage
The message to display if value is empty and the field is required.
The translated string value is read from the message file by default.
Set to "" to use the invalidMessage instead.

### name
Name used when submitting form; same as "name" attribute or plain HTML elements

### ownerDocument
The document this widget belongs to.  If not specified to constructor, will default to
srcNodeRef.ownerDocument, or if no sourceRef specified, then to the document global

### placeHolder
Defines a hint to help users fill out the input field (as defined in HTML 5).
This should only contain plain text (no html markup).

### popupClass
Name of the popup widget class used to select a date/time.
Subclasses should specify this.

### promptMessage
If defined, display this hint string immediately on focus to the textbox, if empty.
Also displays if the textbox value is Incomplete (not yet valid but will be with additional input).
Think of this like a tooltip that tells the user what to do, not an error message
that tells the user what they've done wrong.

Message disappears when user starts typing.

### propercase
Converts the first character of each word to uppercase if true.

### rangeMessage
The message to display if value is out-of-range

### readOnly
Should this widget respond to user input?
In markup, this is specified as "readOnly".
Similar to disabled except readOnly form values are submitted.

### regExp


### required
User is required to enter data into this field.

### scrollOnFocus
On focus, should this widget scroll into view?

### searchContainerNode


### selectOnClick
If true, all text will be selected when focused with mouse

### srcNodeRef
pointer to original DOM node

### state
Shows current state (ie, validation result) of input (""=Normal, Incomplete, or Error)

### style
HTML style attributes as cssText string or name/value hash

### tabIndex
Order fields are traversed when user hits the tab key

### templatePath
Path to template (HTML file) for this widget relative to dojo.baseUrl.
Deprecated: use templateString with require([... "dojo/text!..."], ...) instead

### templateString


### title
HTML title attribute.

For form widgets this specifies a tooltip to display when hovering over
the widget (just like the native HTML title attribute).

For TitlePane or for when this widget is a child of a TabContainer, AccordionContainer,
etc., it's used to specify the tab label, accordion pane title, etc.

### tooltip
When this widget's title attribute is used to for a tab label, accordion pane title, etc.,
this specifies the tooltip to appear when the mouse is hovered over that text.

### tooltipPosition
See description of `dijit/Tooltip.defaultPosition` for details on this parameter.

### trim
Removes leading and trailing whitespace if true.  Default is false.

### type
Corresponds to the native HTML `<input>` element's attribute.

### uppercase
Converts all characters to uppercase if true.  Default is false.

### value
The value of this widget as a JavaScript Date object.  Use get("value") / set("value", val) to manipulate.
When passed to the parser in markup, must be specified according to `dojo/date/stamp.fromISOString()`

## Methods

### attr
Set or get properties on a widget instance.

### buildRendering


### closeDropDown
Closes the drop down on this widget

### compare


### connect
Deprecated, will be removed in 2.0, use this.own(on(...)) or this.own(aspect.after(...)) instead.

Connects specified obj/event to specified method of this object
and registers for disconnect() on widget destroy.

Provide widget-specific analog to dojo.connect, except with the
implicit use of this widget as the target object.
Events connected with `this.connect` are disconnected upon
destruction.

### create
Kick off the life-cycle of a widget

### defer
Wrapper to setTimeout to avoid deferred functions executing
after the originating widget has been destroyed.
Returns an object handle with a remove method (that returns null) (replaces clearTimeout).

### destroy
Destroy this widget, but not its descendants.  Descendants means widgets inside of
this.containerNode.   Will also destroy any resources (including widgets) registered via this.own().

This method will also destroy internal widgets such as those created from a template,
assuming those widgets exist inside of this.domNode but outside of this.containerNode.

For 2.0 it's planned that this method will also destroy descendant widgets, so apps should not
depend on the current ability to destroy a widget without destroying its descendants.   Generally
they should use destroyRecursive() for widgets with children.

### destroyDescendants
Recursively destroy the children of this widget and their
descendants.

### destroyRecursive
Destroy this widget and its descendants

### destroyRendering
Destroys the DOM nodes associated with this widget.

### disconnect
Deprecated, will be removed in 2.0, use handle.remove() instead.

Disconnects handle created by `connect`.

### displayMessage
Overridable method to display validation errors/hints.
By default uses a tooltip.

### emit
Used by widgets to signal that a synthetic event occurred, ex:

    myWidget.emit("attrmodified-selectedChildWidget", {}).


Emits an event on this.domNode named type.toLowerCase(), based on eventObj.
Also calls onType() method, if present, and returns value from that method.
By default passes eventObj to callback, but will pass callbackArgs instead, if specified.
Modifies eventObj by adding missing parameters (bubbles, cancelable, widget).

### filter
Auto-corrections (such as trimming) that are applied to textbox
value on blur or form submit.

### focus
Put focus on this widget

### format
Formats the value as a Date, according to specified locale (second argument)

### get
Get a property from a widget.

### getChildren
Returns all direct children of this widget, i.e. all widgets underneath this.containerNode whose parent
is this widget.   Note that it does not return all descendants, but rather just direct children.
Analogous to [Node.childNodes](https://developer.mozilla.org/en-US/docs/DOM/Node.childNodes),
except containing widgets rather than DOMNodes.

The result intentionally excludes internally created widgets (a.k.a. supporting widgets)
outside of this.containerNode.

Note that the array returned is a simple array.  Application code should not assume
existence of methods like forEach().

### getDescendants
Returns all the widgets contained by this, i.e., all widgets underneath this.containerNode.
This method should generally be avoided as it returns widgets declared in templates, which are
supposed to be internal/hidden, but it's left here for back-compat reasons.

### getDisplayedValue
Deprecated.  Use get('displayedValue') instead.

### getErrorMessage


### getParent
Returns the parent widget of this widget.

### getPromptMessage
Return a hint message to show when widget is first focused

### getValue
Deprecated.  Use get('value') instead.

### isFocusable
Return true if this widget can currently be focused
and false if not

### isInRange
Tests if the value is in the min/max range specified in constraints

### isLeftToRight
Return this widget's explicit or implicit orientation (true for LTR, false for RTL)

### isLoaded
Returns true if the dropdown exists and it's data is loaded.  This can
be overridden in order to force a call to loadDropDown().

### isValid


### loadAndOpenDropDown
Creates the drop down if it doesn't exist, loads the data
if there's an href and it hasn't been loaded yet, and
then opens the drop down.  This is basically a callback when the
user presses the down arrow button to open the drop down.

### loadDropDown
Creates the drop down if it doesn't exist, loads the data
if there's an href and it hasn't been loaded yet, and then calls
the given callback.

### on


### onBlur
Called when the widget stops being "active" because
focus moved to something outside of it, or the user
clicked somewhere outside of it, or the widget was
hidden.

### onChange
Callback when this widget's value is changed.

### onClick
Connect to this function to receive notifications of mouse click events.

### onClose
Called when this widget is being displayed as a popup (ex: a Calendar popped
up from a DateTextBox), and it is hidden.
This is called from the dijit.popup code, and should not be called directly.

Also used as a parameter for children of `dijit/layout/StackContainer` or subclasses.
Callback if a user tries to close the child.   Child will be closed if this function returns true.

### onDblClick
Connect to this function to receive notifications of mouse double click events.

### onFocus
Called when the widget becomes "active" because
it or a widget inside of it either has focus, or has recently
been clicked.

### onHide
Called when another widget becomes the selected pane in a
`dijit/layout/TabContainer`, `dijit/layout/StackContainer`,
`dijit/layout/AccordionContainer`, etc.

Also called to indicate hide of a `dijit.Dialog`, `dijit.TooltipDialog`, or `dijit.TitlePane`.

### onInput
Connect to this function to receive notifications of various user data-input events.
Return false to cancel the event and prevent it from being processed.

### onKeyDown
Connect to this function to receive notifications of keys being pressed down.

### onKeyPress
Connect to this function to receive notifications of printable keys being typed.

### onKeyUp
Connect to this function to receive notifications of keys being released.

### onMouseDown
Connect to this function to receive notifications of when the mouse button is pressed down.

### onMouseEnter
Connect to this function to receive notifications of when the mouse moves onto this widget.

### onMouseLeave
Connect to this function to receive notifications of when the mouse moves off of this widget.

### onMouseMove
Connect to this function to receive notifications of when the mouse moves over nodes contained within this widget.

### onMouseOut
Connect to this function to receive notifications of when the mouse moves off of nodes contained within this widget.

### onMouseOver
Connect to this function to receive notifications of when the mouse moves onto nodes contained within this widget.

### onMouseUp
Connect to this function to receive notifications of when the mouse button is released.

### onShow
Called when this widget becomes the selected pane in a
`dijit/layout/TabContainer`, `dijit/layout/StackContainer`,
`dijit/layout/AccordionContainer`, etc.

Also called to indicate display of a `dijit.Dialog`, `dijit.TooltipDialog`, or `dijit.TitlePane`.

### openDropDown


### own
Track specified handles and remove/destroy them when this instance is destroyed, unless they were
already removed/destroyed manually.

### parse
Parses as string as a Date, according to constraints

### pattern
Builds the regular needed to parse a localized date

### placeAt
Place this widget somewhere in the DOM based
on standard domConstruct.place() conventions.

### postCreate


### postMixInProperties


### postscript
Kicks off widget instantiation.  See create() for details.

### rangeCheck
Overridable function used to validate the range of the numeric input value.

### regExpGen
Deprecated.  Use set('pattern', Function) instead.

### reset


### serialize


### set
Set a property on a widget

### setAttribute
Deprecated.  Use set() instead.

### setDisabled
Deprecated.  Use set('disabled', ...) instead.

### setDisplayedValue
Deprecated.  Use set('displayedValue', ...) instead.

### setValue
Deprecated.  Use set('value', ...) instead.

### startup


### subscribe
Deprecated, will be removed in 2.0, use this.own(topic.subscribe()) instead.

Subscribes to the specified topic and calls the specified method
of this object and registers for unsubscribe() on widget destroy.

Provide widget-specific analog to dojo.subscribe, except with the
implicit use of this widget as the target object.

### toggleDropDown
Callback when the user presses the down arrow button or presses
the down arrow key to open/close the drop down.
Toggle the drop-down widget; if it is up, close it, if not, open it

### undo
Restore the value to the last value passed to onChange

### uninitialize
Deprecated. Override destroy() instead to implement custom widget tear-down
behavior.

### unsubscribe
Deprecated, will be removed in 2.0, use handle.remove() instead.

Unsubscribes handle created by this.subscribe.
Also removes handle from this widget's list of subscriptions

### validate


### validator
Overridable function used to validate the text input against the regular expression.

### watch
Watches a property for changes

