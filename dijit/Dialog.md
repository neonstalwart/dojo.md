# Module: dijit/Dialog

*Constructor*

# Constructor

## Summary

A modal dialog Widget.
## Description

Pops up a modal dialog window, blocking access to the screen
and also graying out the screen Dialog is extended from
ContentPane so it supports all the same parameters (href, etc.).
## Examples

*       <div data-dojo-type="dijit/Dialog" data-dojo-props="href: 'test.html'"></div>
*       var foo = new Dialog({ title: "test dialog", content: "test content" });
      foo.placeAt(win.body());
      foo.startup();


## Properties

### active
True if mouse was pressed while over this widget, and hasn't been released yet

### aria-describedby


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

### autofocus
A Toggle to modify the default focus behavior of a Dialog, which
is to focus on the first dialog element after opening the dialog.
False will disable autofocusing. Default: true

### baseClass


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

### content
The innerHTML of the ContentPane.
Note that the initialization parameter / argument to set("content", ...)
can be a String, DomNode, Nodelist, or _Widget.

### cssStateNodes


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

### draggable
Toggles the moveable aspect of the Dialog. If true, Dialog
can be dragged by it's title. If false it will remain centered
in the viewport.

### duration
The time in milliseconds it takes the dialog to fade in and out

### errorMessage
Message that shows if an error occurs

### extractContent
Extract visible content from inside of `<body> .... </body>`.
I.e., strip `<html>` and `<head>` (and it's contents) from the href

### focused
This widget or a widget it contains has focus, or is "active" because
it was recently clicked.

### hovering
True if cursor is over this widget

### href
The href of the content that displays now.
Set this at construction if you want to load data externally when the
pane is shown.  (Set preload=true to load it immediately.)
Changing href after creation doesn't have any effect; Use set('href', ...);

### id
A unique, opaque ID string that can be assigned by users or by the
system. If the developer passes an ID which is known not to be
unique, the specified ID is ignored and the system-generated ID is
used instead.

### ioArgs
Parameters to pass to xhrGet() request, for example:

      <div data-dojo-type="dijit/layout/ContentPane" data-dojo-props="href: './bar', ioArgs: {timeout: 500}">

### isLayoutContainer
Indicates that this widget will call resize() on it's child widgets
when they become visible.

### isLoaded
True if the ContentPane has data in it, either specified
during initialization (via href or inline content), or set
via set('content', ...) / set('href', ...)

False if it doesn't have any content, or if ContentPane is
still in the process of downloading href.

### lang
Rarely used.  Overrides the default Dojo locale used to render this widget,
as defined by the [HTML LANG](http://www.w3.org/TR/html401/struct/dirlang.html#adef-lang) attribute.
Value must be among the list of locales specified during by the Dojo bootstrap,
formatted according to [RFC 3066](http://www.ietf.org/rfc/rfc3066.txt) (like en-us).

### loadingMessage
Message that shows while downloading

### maxRatio
Maximum size to allow the dialog to expand to, relative to viewport size

### onLoadDeferred
This is the `dojo.Deferred` returned by set('href', ...) and refresh().
Calling onLoadDeferred.then() registers your
callback to be called only once, when the prior set('href', ...) call or
the initial href parameter to the constructor finishes loading.

This is different than an onLoad() handler which gets called any time any href
or content is loaded.

### open
True if Dialog is currently displayed on screen.

### ownerDocument
The document this widget belongs to.  If not specified to constructor, will default to
srcNodeRef.ownerDocument, or if no sourceRef specified, then to the document global

### parseOnLoad
Parse content and create the widgets, if any.

### parserScope
Flag passed to parser.  Root for attribute names to search for.   If scopeName is dojo,
will search for data-dojo-type (or dojoType).  For backwards compatibility
reasons defaults to dojo._scopeName (which is "dojo" except when
multi-version support is used, when it will be something like dojo16, dojo20, etc.)

### preload
Force load of data on initialization even if pane is hidden.

### preventCache
Prevent caching of data from href's by appending a timestamp to the href.

### refocus
A Toggle to modify the default focus behavior of a Dialog, which
is to re-focus the element which had focus before being opened.
False will disable refocusing. Default: true

### refreshOnShow
Refresh (re-download) content when pane goes from hidden to shown

### searchContainerNode


### srcNodeRef
pointer to original DOM node

### state
Will be "Error" if one or more of the child widgets has an invalid value,
"Incomplete" if not all of the required child widgets are filled in.  Otherwise, "",
which indicates that the form is ready to be submitted.

### stopParser


### style
HTML style attributes as cssText string or name/value hash

### template
Flag from the parser that this ContentPane is inside a template
so the contents are pre-parsed.

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

### attr
Set or get properties on a widget instance.

### buildRendering


### cancel
Cancels an in-flight download of content

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


### defer
Wrapper to setTimeout to avoid deferred functions executing
after the originating widget has been destroyed.
Returns an object handle with a remove method (that returns null) (replaces clearTimeout).

### destroy


### destroyDescendants
Destroy all the widgets inside the ContentPane and empty containerNode

### destroyRecursive
Destroy the ContentPane and its contents

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
Callback when the user hits the submit button.
Override this method to handle Dialog execution.

### focus


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

### getValues


### hasChildren
Returns true if widget has child widgets, i.e. if this.containerNode contains widgets.

### hide
Hide the dialog

### ioMethod
Function that should grab the content specified via href.

### isFocusable
Return true if this widget can currently be focused
and false if not

### isLeftToRight
Return this widget's explicit or implicit orientation (true for LTR, false for RTL)

### isValid
Returns true if all of the widgets are valid.
Deprecated, will be removed in 2.0.  Use get("state") instead.

### markupFactory


### on


### onBlur
Called when the widget stops being "active" because
focus moved to something outside of it, or the user
clicked somewhere outside of it, or the widget was
hidden.

### onCancel
Called when user has pressed the Dialog's cancel button, to notify container.

### onClick
Connect to this function to receive notifications of mouse click events.

### onClose
Called when this widget is being displayed as a popup (ex: a Calendar popped
up from a DateTextBox), and it is hidden.
This is called from the dijit.popup code, and should not be called directly.

Also used as a parameter for children of `dijit/layout/StackContainer` or subclasses.
Callback if a user tries to close the child.   Child will be closed if this function returns true.

### onContentError
Called on DOM faults, require faults etc. in content.

In order to display an error message in the pane, return
the error message from this method, as an HTML string.

By default (if this method is not overriden), it returns
nothing, so the error message is just printed to the console.

### onDblClick
Connect to this function to receive notifications of mouse double click events.

### onDownloadEnd
Called when download is finished.

### onDownloadError
Called when download error occurs.

In order to display an error message in the pane, return
the error message from this method, as an HTML string.

Default behavior (if this method is not overriden) is to display
the error message inside the pane.

### onDownloadStart
Called before download starts.

### onExecute
Called when user has pressed the dialog's OK button, to notify container.

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

### onLoad
Event hook, is called after everything is loaded and widgetified

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

### onUnload
Event hook, is called before old content is cleared

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

### refresh
[Re]download contents of href and display

### removeChild
Removes the passed widget instance from this widget but does
not destroy it.  You can also pass in an integer indicating
the index within the container to remove (ie, removeChild(5) removes the sixth widget).

### reset


### resize
See `dijit/layout/_LayoutWidget.resize()` for description.
Although ContentPane doesn't extend _LayoutWidget, it does implement
the same API.

### set
Set a property on a widget

### setAttribute
Deprecated.  Use set() instead.

### setContent
Deprecated.   Use set('content', ...) instead.

### setHref
Deprecated.   Use set('href', ...) instead.

### setValues


### show
Display the dialog

### startup
Call startup() on all children including non _Widget ones like dojo/dnd/Source objects

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

