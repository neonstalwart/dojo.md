# Module: dijit/form/Form

*Constructor*

# Constructor

## Summary

Widget corresponding to HTML form tag, for validation and serialization

## Examples

      <form data-dojo-type="dijit/form/Form" id="myForm">
        Name: <input type="text" name="name" />
      </form>
      myObj = {name: "John Doe"};
      dijit.byId('myForm').set('value', myObj);
    
      myObj=dijit.byId('myForm').get('value');
## Properties

### accept
List of MIME types for file upload.

### accept-charset


### action
Server-side form handler.

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

### declaredClass


### dir
Bi-directional support, as defined by the [HTML DIR](http://www.w3.org/TR/html401/struct/dirlang.html#adef-dir)
attribute. Either left-to-right "ltr" or right-to-left "rtl".  If undefined, widgets renders in page's
default direction.

### doLayout
- false - don't adjust size of children
- true - if there is a single visible child widget, set it's size to however big the ContentPane is

### domNode
This is our visible representation of the widget! Other DOM
Nodes may by assigned to other properties, usually through the
template system's data-dojo-attach-point syntax, but the domNode
property is the canonical "top level" node in widget UI.

### encType
Encoding type for the form, ex: application/x-www-form-urlencoded.

### focused
This widget or a widget it contains has focus, or is "active" because
it was recently clicked.

### id
A unique, opaque ID string that can be assigned by users or by the
system. If the developer passes an ID which is known not to be
unique, the specified ID is ignored and the system-generated ID is
used instead.

### isLayoutContainer
Indicates that this widget will call resize() on it's child widgets
when they become visible.

### lang
Rarely used.  Overrides the default Dojo locale used to render this widget,
as defined by the [HTML LANG](http://www.w3.org/TR/html401/struct/dirlang.html#adef-lang) attribute.
Value must be among the list of locales specified during by the Dojo bootstrap,
formatted according to [RFC 3066](http://www.ietf.org/rfc/rfc3066.txt) (like en-us).

### method
HTTP method used to submit the form, either "GET" or "POST".

### name
Name of form for scripting.

### ownerDocument
The document this widget belongs to.  If not specified to constructor, will default to
srcNodeRef.ownerDocument, or if no sourceRef specified, then to the document global

### searchContainerNode


### srcNodeRef
pointer to original DOM node

### state
Will be "Error" if one or more of the child widgets has an invalid value,
"Incomplete" if not all of the required child widgets are filled in.  Otherwise, "",
which indicates that the form is ready to be submitted.

### style
HTML style attributes as cssText string or name/value hash

### target
Target frame for the document to be opened in.

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

## Methods

### attr
Set or get properties on a widget instance.

### buildRendering
Construct the UI for this widget, setting this.domNode.
Most widgets will mixin `dijit._TemplatedMixin`, which implements this method.

### connect
Deprecated, will be removed in 2.0, use this.own(on(...)) or this.own(aspect.after(...)) instead.

Connects specified obj/event to specified method of this object
and registers for disconnect() on widget destroy.

Provide widget-specific analog to dojo.connect, except with the
implicit use of this widget as the target object.
Events connected with `this.connect` are disconnected upon
destruction.

### connectChildren
You can call this function directly, ex. in the event that you
programmatically add a widget to the form *after* the form has been
initialized.

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

### disconnectChildren
Deprecated method.   Applications no longer need to call this.   Remove for 2.0.

### emit
Used by widgets to signal that a synthetic event occurred, ex:

      myWidget.emit("attrmodified-selectedChildWidget", {}).


Emits an event on this.domNode named type.toLowerCase(), based on eventObj.
Also calls onType() method, if present, and returns value from that method.
By default passes eventObj to callback, but will pass callbackArgs instead, if specified.
Modifies eventObj by adding missing parameters (bubbles, cancelable, widget).

### execute
Deprecated: use submit()

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

### getParent
Returns the parent widget of this widget.

### getValues


### isFocusable
Return true if this widget can currently be focused
and false if not

### isLeftToRight
Return this widget's explicit or implicit orientation (true for LTR, false for RTL)

### isValid
Returns true if all of the widgets are valid.
Deprecated, will be removed in 2.0.  Use get("state") instead.

### on


### onBlur
Called when the widget stops being "active" because
focus moved to something outside of it, or the user
clicked somewhere outside of it, or the widget was
hidden.

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

### onExecute
Deprecated: use onSubmit()

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

### onReset
Callback when user resets the form. This method is intended
to be over-ridden. When the `reset` method is called
programmatically, the return value from `onReset` is used
to compute whether or not resetting should proceed

### onShow
Called when this widget becomes the selected pane in a
`dijit/layout/TabContainer`, `dijit/layout/StackContainer`,
`dijit/layout/AccordionContainer`, etc.

Also called to indicate display of a `dijit.Dialog`, `dijit.TooltipDialog`, or `dijit.TitlePane`.

### onSubmit
Callback when user submits the form.

### onValidStateChange
Stub function to connect to if you want to do something
(like disable/enable a submit button) when the valid
state changes on the form as a whole.

Deprecated.  Will be removed in 2.0.  Use watch("state", ...) instead.

### own
Track specified handles and remove/destroy them when this instance is destroyed, unless they were
already removed/destroyed manually.

### placeAt
Place this widget somewhere in the DOM based
on standard domConstruct.place() conventions.

### postCreate


### postMixInProperties


### postscript
Kicks off widget instantiation.  See create() for details.

### reset
restores all widget values back to their init values,
calls onReset() which can cancel the reset by returning false

### resize
See `dijit/layout/_LayoutWidget.resize()` for description.
Although ContentPane doesn't extend _LayoutWidget, it does implement
the same API.

### set
Set a property on a widget

### setAttribute
Deprecated.  Use set() instead.

### setValues


### startup
Processing after the DOM fragment is added to the document

### submit
programmatically submit form if and only if the `onSubmit` returns true

### subscribe
Deprecated, will be removed in 2.0, use this.own(topic.subscribe()) instead.

Subscribes to the specified topic and calls the specified method
of this object and registers for unsubscribe() on widget destroy.

Provide widget-specific analog to dojo.subscribe, except with the
implicit use of this widget as the target object.

### uninitialize
Deprecated. Override destroy() instead to implement custom widget tear-down
behavior.

### unsubscribe
Deprecated, will be removed in 2.0, use handle.remove() instead.

Unsubscribes handle created by this.subscribe.
Also removes handle from this widget's list of subscriptions

### validate
returns if the form is valid - same as isValid - but
provides a few additional (ui-specific) features:

1. it will highlight any sub-widgets that are not valid
2. it will call focus() on the first invalid sub-widget

### watch
Watches a property for changes

