# Module: dijit/form/_FormSelectWidget

*Constructor*

# Constructor

## Summary

Extends _FormValueWidget in order to provide "select-specific"
values - i.e., those values that are unique to `<select>` elements.
This also provides the mechanism for reading the elements from
a store, if desired.
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

### baseClass
Root CSS class of the widget (ex: dijitTextBox), used to construct CSS classes to indicate
widget state.

### class


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
Subclasses may define a cssStateNodes property that lists sub-nodes within the widget that
need CSS classes applied on mouse hover/press and focus.

Each entry in this optional hash is a an attach-point name (like "upArrowButton") mapped to a CSS class name
(like "dijitUpArrowButton"). Example:

        {
          "upArrowButton": "dijitUpArrowButton",
          "downArrowButton": "dijitDownArrowButton"
        }

The above will set the CSS class dijitUpArrowButton to the this.upArrowButton DOMNode when it
is hovered, etc.

### declaredClass


### dir
Bi-directional support, as defined by the [HTML DIR](http://www.w3.org/TR/html401/struct/dirlang.html#adef-dir)
attribute. Either left-to-right "ltr" or right-to-left "rtl".  If undefined, widgets renders in page's
default direction.

### disabled
Should this widget respond to user input?
In markup, this is specified as "disabled='disabled'", or just "disabled".

### domNode
This is our visible representation of the widget! Other DOM
Nodes may by assigned to other properties, usually through the
template system's data-dojo-attach-point syntax, but the domNode
property is the canonical "top level" node in widget UI.

### focused
This widget or a widget it contains has focus, or is "active" because
it was recently clicked.

### hovering
True if cursor is over this widget

### id
A unique, opaque ID string that can be assigned by users or by the
system. If the developer passes an ID which is known not to be
unique, the specified ID is ignored and the system-generated ID is
used instead.

### intermediateChanges
Fires onChange for each value change or only on demand

### labelAttr
The entries in the drop down list come from this attribute in the dojo.store items.
If ``store`` is set, labelAttr must be set too, unless store is an old-style
dojo.data store rather than a new dojo/store.

### lang
Rarely used.  Overrides the default Dojo locale used to render this widget,
as defined by the [HTML LANG](http://www.w3.org/TR/html401/struct/dirlang.html#adef-lang) attribute.
Value must be among the list of locales specified during by the Dojo bootstrap,
formatted according to [RFC 3066](http://www.ietf.org/rfc/rfc3066.txt) (like en-us).

### loadChildrenOnOpen
By default loadChildren is called when the items are fetched from the
store.  This property allows delaying loadChildren (and the creation
of the options/menuitems) until the user clicks the button to open the
dropdown.

### multiple
Whether or not we are multi-valued

### name
Name used when submitting form; same as "name" attribute or plain HTML elements

### onFetch
A callback to do with an onFetch - but before any items are actually
iterated over (i.e. to filter even further what you want to add)

### onLoadDeferred
This is the `dojo.Deferred` returned by setStore().
Calling onLoadDeferred.then() registers your
callback to be called only once, when the prior setStore completes.

### options
The set of options for our select item.  Roughly corresponds to
the html `<option>` tag.

### ownerDocument
The document this widget belongs to.  If not specified to constructor, will default to
srcNodeRef.ownerDocument, or if no sourceRef specified, then to the document global

### query
A query to use when fetching items from our store

### queryOptions
Query options to use when fetching from the store

### readOnly
Should this widget respond to user input?
In markup, this is specified as "readOnly".
Similar to disabled except readOnly form values are submitted.

### scrollOnFocus
On focus, should this widget scroll into view?

### searchContainerNode


### sortByLabel
Flag to sort the options returned from a store by the label of
the store.

### srcNodeRef
pointer to original DOM node

### store
A store to use for getting our list of options - rather than reading them
from the `<option>` html tags.   Should support getIdentity().
For back-compat store can also be a dojo/data/api/Identity.

### style
HTML style attributes as cssText string or name/value hash

### tabIndex
Order fields are traversed when user hits the tab key

### templatePath
Path to template (HTML file) for this widget relative to dojo.baseUrl.
Deprecated: use templateString with require([... "dojo/text!..."], ...) instead

### templateString
A string that represents the widget template.
Use in conjunction with dojo.cache() to load from a file.

### title
HTML title attribute.

For form widgets this specifies a tooltip to display when hovering over
the widget (just like the native HTML title attribute).

For TitlePane or for when this widget is a child of a TabContainer, AccordionContainer,
etc., it's used to specify the tab label, accordion pane title, etc.

### tooltip
When this widget's title attribute is used to for a tab label, accordion pane title, etc.,
this specifies the tooltip to appear when the mouse is hovered over that text.

### type
Corresponds to the native HTML `<input>` element's attribute.

### value
Corresponds to the native HTML `<input>` element's attribute.

## Methods

### addOption
Adds an option or options to the end of the select.  If value
of the option is empty or missing, a separator is created instead.
Passing in an array of options will yield slightly better performance
since the children are only loaded once.

### attr
Set or get properties on a widget instance.

### buildRendering


### compare
Compare 2 values (as returned by get('value') for this widget).

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
Clean up our connections

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

### emit
Used by widgets to signal that a synthetic event occurred, ex:

      myWidget.emit("attrmodified-selectedChildWidget", {}).


Emits an event on this.domNode named type.toLowerCase(), based on eventObj.
Also calls onType() method, if present, and returns value from that method.
By default passes eventObj to callback, but will pass callbackArgs instead, if specified.
Modifies eventObj by adding missing parameters (bubbles, cancelable, widget).

### focus
Put focus on this widget

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

### getOptions
Returns a given option (or options).

### getParent
Returns the parent widget of this widget.

### getValue
Deprecated.  Use get('value') instead.

### isFocusable
Return true if this widget can currently be focused
and false if not

### isLeftToRight
Return this widget's explicit or implicit orientation (true for LTR, false for RTL)

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

### onSetStore
a function that can be connected to in order to receive a
notification that the store has finished loading and all options
from that store are available

### onShow
Called when this widget becomes the selected pane in a
`dijit/layout/TabContainer`, `dijit/layout/StackContainer`,
`dijit/layout/AccordionContainer`, etc.

Also called to indicate display of a `dijit.Dialog`, `dijit.TooltipDialog`, or `dijit.TitlePane`.

### own
Track specified handles and remove/destroy them when this instance is destroyed, unless they were
already removed/destroyed manually.

### placeAt
Place this widget somewhere in the DOM based
on standard domConstruct.place() conventions.

### postCreate
sets up our event handling that we need for functioning
as a select

### postMixInProperties


### postscript
Kicks off widget instantiation.  See create() for details.

### removeOption
Removes the given option or options.  You can remove by string
(in which case the value is removed), number (in which case the
index in the options array is removed), or select option (in
which case, the select option with a matching value is removed).
You can also pass in an array of those values for a slightly
better performance since the children are only loaded once.
For numeric option values, specify {value: number} as the argument.

### reset
Reset the widget's value to what it was at initialization time

### set
Set a property on a widget

### setAttribute
Deprecated.  Use set() instead.

### setDisabled
Deprecated.  Use set('disabled', ...) instead.

### setStore
Sets the store you would like to use with this select widget.
The selected value is the value of the new store to set.  This
function returns the original store, in case you want to reuse
it or something.

### setValue
Deprecated.  Use set('value', ...) instead.

### startup


### subscribe
Deprecated, will be removed in 2.0, use this.own(topic.subscribe()) instead.

Subscribes to the specified topic and calls the specified method
of this object and registers for unsubscribe() on widget destroy.

Provide widget-specific analog to dojo.subscribe, except with the
implicit use of this widget as the target object.

### undo
Restore the value to the last value passed to onChange

### uninitialize
Deprecated. Override destroy() instead to implement custom widget tear-down
behavior.

### unsubscribe
Deprecated, will be removed in 2.0, use handle.remove() instead.

Unsubscribes handle created by this.subscribe.
Also removes handle from this widget's list of subscriptions

### updateOption
Updates the values of the given option.  The option to update
is matched based on the value of the entered option.  Passing
in an array of new options will yield better performance since
the children will only be loaded once.

### watch
Watches a property for changes

