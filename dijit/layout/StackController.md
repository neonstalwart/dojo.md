# Module: dijit/layout/StackController

*Constructor*

## Properties

### StackButton


# Constructor

## Summary

Set of buttons to select a page in a `dijit/layout/StackContainer`
## Description

Monitors the specified StackContainer, and whenever a page is
added, deleted, or selected, updates itself accordingly.
## Properties

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


### buttonWidget
The button widget to create to correspond to each page

### buttonWidgetCloseClass
CSS class of [x] close icon, used by event delegation code to tell when close button was clicked

### class


### containerId
The id of the page container that I point to

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

### domNode
This is our visible representation of the widget! Other DOM
Nodes may by assigned to other properties, usually through the
template system's data-dojo-attach-point syntax, but the domNode
property is the canonical "top level" node in widget UI.

### focused
This widget or a widget it contains has focus, or is "active" because
it was recently clicked.

### id
A unique, opaque ID string that can be assigned by users or by the
system. If the developer passes an ID which is known not to be
unique, the specified ID is ignored and the system-generated ID is
used instead.

### lang
Rarely used.  Overrides the default Dojo locale used to render this widget,
as defined by the [HTML LANG](http://www.w3.org/TR/html401/struct/dirlang.html#adef-lang) attribute.
Value must be among the list of locales specified during by the Dojo bootstrap,
formatted according to [RFC 3066](http://www.ietf.org/rfc/rfc3066.txt) (like en-us).

### ownerDocument
The document this widget belongs to.  If not specified to constructor, will default to
srcNodeRef.ownerDocument, or if no sourceRef specified, then to the document global

### searchContainerNode


### srcNodeRef
pointer to original DOM node

### style
HTML style attributes as cssText string or name/value hash

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

### addChild
Makes the given widget a child of this widget.

### adjacent
Helper for onkeydown to find next/previous button

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

### create
Kick off the life-cycle of a widget

### defer
Wrapper to setTimeout to avoid deferred functions executing
after the originating widget has been destroyed.
Returns an object handle with a remove method (that returns null) (replaces clearTimeout).

### destroy


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

### getIndexOfChild
Gets the index of the child in this container or -1 if not found

### getParent
Returns the parent widget of this widget.

### hasChildren
Returns true if widget has child widgets, i.e. if this.containerNode contains widgets.

### isFocusable
Return true if this widget can currently be focused
and false if not

### isLeftToRight
Return this widget's explicit or implicit orientation (true for LTR, false for RTL)

### on


### onAddChild
Called whenever a page is added to the container.
Create button corresponding to the page.

### onBlur
Called when the widget stops being "active" because
focus moved to something outside of it, or the user
clicked somewhere outside of it, or the widget was
hidden.

### onButtonClick
Called whenever one of my child buttons is pressed in an attempt to select a page

### onClick
Connect to this function to receive notifications of mouse click events.

### onClose
Called when this widget is being displayed as a popup (ex: a Calendar popped
up from a DateTextBox), and it is hidden.
This is called from the dijit.popup code, and should not be called directly.

Also used as a parameter for children of `dijit/layout/StackContainer` or subclasses.
Callback if a user tries to close the child.   Child will be closed if this function returns true.

### onCloseButtonClick
Called whenever one of my child buttons [X] is pressed in an attempt to close a page

### onContainerKeyDown
Called when there was a keydown on the container

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

### onRemoveChild
Called whenever a page is removed from the container.
Remove the button corresponding to the page.

### onSelectChild
Called when a page has been selected in the StackContainer, either by me or by another StackController

### onShow
Called when this widget becomes the selected pane in a
`dijit/layout/TabContainer`, `dijit/layout/StackContainer`,
`dijit/layout/AccordionContainer`, etc.

Also called to indicate display of a `dijit.Dialog`, `dijit.TooltipDialog`, or `dijit.TitlePane`.

### onStartup
Called after StackContainer has finished initializing

### onkeydown
Handle keystrokes on the page list, for advancing to next/previous button
and closing the current page if the page is closable.

### own
Track specified handles and remove/destroy them when this instance is destroyed, unless they were
already removed/destroyed manually.

### pane2button
Returns the button corresponding to the pane w/the given id.

### placeAt
Place this widget somewhere in the DOM based
on standard domConstruct.place() conventions.

### postCreate


### postMixInProperties
Called after the parameters to the widget have been read-in,
but before the widget template is instantiated. Especially
useful to set properties that are referenced in the widget
template.

### postscript
Kicks off widget instantiation.  See create() for details.

### removeChild
Removes the passed widget instance from this widget but does
not destroy it.  You can also pass in an integer indicating
the index within the container to remove (ie, removeChild(5) removes the sixth widget).

### set
Set a property on a widget

### setAttribute
Deprecated.  Use set() instead.

### startup
Processing after the DOM fragment is added to the document

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

### watch
Watches a property for changes

